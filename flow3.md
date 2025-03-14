``` mermaid
---
title: 'Flow 3 - Evaluating Error: Signal vs Noise'
---
    graph TD;
    A[Model<br>'A simplified story about data'] --> B(Data<br>'Composed of Signal + Noise');
    B --> C[Signal<br>'Real, repeatable pattern<br>Goal to capture and generalize'];
    B --> D[Noise<br>'Imperfections, extraneous variation<br>Obscures the signal'] ;
    A --> E[Goal of Modeling<br>'Describe signal, ignore noise'];
    E --> F[Challenges];
    F --> G[Bias<br>'Failure to capture all signal<br>Underfitting'];
    G --> H('Example: Linear model<br>High bias, misses pattern');
    F --> I[Variance<br>'Capturing noise instead of signal<br>Overfitting'];
    I --> J('Example: Connect-the-dots<br>High variance, fits noise');
    E --> K[Solutions];
    K --> L[Against Bias<br>'Try various model types<br>Rich pool of candidates'];
    K --> M[Against Variance<br>'Test generalization<br>Train vs. Test data split'];
    M --> N('Good model: Accurate predictions<br>Low variance, captures signal');
    M --> O('Overfitted model: Poor predictions<br>High variance, captures noise');
    P[Next Step<br>'Choosing the right error function'] --> E;
```
