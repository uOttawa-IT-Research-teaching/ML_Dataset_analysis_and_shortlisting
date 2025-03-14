``` mermaid
---
title: 'Flow 4 - The Problem Domain: Chosing the Model'
---
        flowchart TD;
	    start[Start: Data Science Project] --> problem_type{Select Problem Domain};
        click start href "https://www.github.com" "This is a link" _blank
	    %% Problem Type Branching;
	    problem_type -->|Supervised Learning| supervised{Supervised Learning};
	    problem_type -->|Unsupervised Learning| unsupervised{Unsupervised Learning};
	    problem_type -->|Natural Language| nlp_domain{NLP Tasks};
	    problem_type -->|Computer Vision| vision_domain{Vision Tasks};
        click problem_type href "http://localhost:8890/notebooks/Documents/ML_Notebooks/flowchart2.ipynb" "This is a link" _blank
         
	    %% Supervised Learning Paths;
	    supervised -->|Classification| classification{Classification Complexity};
	    supervised -->|Regression| regression{Regression Complexity};
        click supervised call callback() "Tooltip for a callback"
	    
	    %% Classification Algorithms;
	    classification -->|Small Dataset| simple_classification[/Simple Classification/];
	    classification -->|Complex Dataset| advanced_classification[/Advanced Classification/];
	    
	    simple_classification --> KNN["K-Nearest Neighbors (KNN);
	    Distance-based classification;
	    Works with small datasets;
	    Low computational complexity"];
	    
	    simple_classification --> NaiveBayes["Naive Bayes;
	    Probabilistic classifier;
	    Fast training;
	    Works with categorical data"];
	    
	    advanced_classification --> SVM["Support Vector Machines (SVM);
	    Finds optimal separation hyperplane;
	    Effective in high-dimensional spaces;
	    Complex decision boundaries"];

            
	    advanced_classification --> RandomForest["Random Forest;
	    Ensemble of decision trees;
	    Handles complex relationships;
	    Reduces overfitting;
	    High accuracy"];
	    
	    %% Regression Paths;
	    regression --> DecisionTrees["Decision Trees;
	    Handles non-linear relationships;
	    Captures complex interactions;
	    Interpretable results"];
	    
	    %% NLP Domain;
	    nlp_domain -->|Text Classification| nlp_classification["Traditional NLP Techniques;
	    Naive Bayes;
	    SVM"];
	    
	    nlp_domain -->|Advanced Language Tasks| advanced_nlp{Advanced NLP};
	    
	    advanced_nlp -->|Large Language Models| LLM["Large Language Models (LLM)
	    Transformer-based;
	    Contextual understanding;
	    Generative capabilities"];
	    
	    advanced_nlp -->|Transfer Learning| TransferLearning["Transfer Learning
	    Leverage pre-trained models;
	    Reduce training time;
	    Effective with limited data"];
	    
	    %% Computer Vision;
	    vision_domain -->|Feature Extraction| CNN["Convolutional Neural Networks (CNN)
	    Specialized image processing;
	    Learns hierarchical features;
	    State-of-the-art computer vision"];
	    
	    vision_domain -->|Complex Visual Tasks| DNN["Deep Neural Networks (DNN)
	    Multiple hidden layers;
	    Complex pattern recognition;
	    Versatile architecture"];
	    
	    %% Unsupervised Learning;
	    unsupervised -->|Clustering| clustering["Clustering Algorithms
	    K-Means;
	    Hierarchical Clustering;
	    DBSCAN"];
	    
	    unsupervised -->|Dimensionality Reduction| dim_reduction["Dimensionality Reduction
	    PCA;
	    t-SNE;
	    UMAP"];
	    
	    %% Model Inference and Deployment;
	    KNN & NaiveBayes & SVM & RandomForest & DecisionTrees &  LLM & TransferLearning & CNN & DNN --> inference{Model Inference};
	    inference -->|Deployment Preparation| ModelDeployment["Model Deployment
	    Performance optimization
	    Real-world prediction
	    Scalable inference"];
	    
	    %% Styling
	    classDef decision fill:#f9e79f,stroke:#d35400;
	    classDef algorithm fill:#d4edda,stroke:#155724;
	    classDef deployment fill:#f2f3f4,stroke:#2c3e50;
	    class problem_type,supervised,unsupervised,nlp_domain,vision_domain,classification,regression,advanced_nlp,inference decision;
	    class KNN,NaiveBayes,SVM,RandomForest,DecisionTrees,LLM,TransferLearning,CNN,DNN algorithm;
	    class ModelDeployment deployment;
```
