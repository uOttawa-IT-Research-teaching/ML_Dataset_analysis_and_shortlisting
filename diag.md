<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mermaid Diagram with Zoom and Pan</title>
    <style>
        #graphDiv {
            height: 90vh;
            width: 100%;
        }
    </style>
</head>
<body>
    <div id="graphDiv"></div>
    <script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/svg-pan-zoom/3.6.1/svg-pan-zoom.min.js"></script>
    <script>
        mermaid.initialize({ startOnLoad: true });

        document.addEventListener('DOMContentLoaded', () => {
            const graphDefinition = `
                graph TD;
                A-->B;
                A-->C;
                B-->D;
                C-->D;
            `;
            mermaid.render('graphDiv', graphDefinition, (svgCode) => {
                document.getElementById('graphDiv').innerHTML = svgCode;
                svgPanZoom('#graphDiv svg', {
                    zoomEnabled: true,
                    controlIconsEnabled: true
                });
            });
        });
    </script>
</body>
</html>
