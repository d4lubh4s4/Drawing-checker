<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <title>Drawing PDF Checker</title>  
  <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>  
  <style>  
    body { font-family: Arial, sans-serif; margin: 20px; }  
    h1 { font-size: 1.5rem; }  
    .controls { margin-bottom: 20px; }  
    label { display: block; margin-top: 10px; }  
    input[type="text"] { width: 100%; padding: 6px; }  
    button { margin-top: 15px; padding: 10px 16px; cursor: pointer; }  
    canvas { border: 1px solid #ccc; margin-top: 20px; max-width: 100%; }  
    .results { margin-top: 20px; }  
    .ok { color: green; }  
    .bad { color: red; }  
  </style>  
</head>  
<body>  
  <h1>Drawing PDF Checker</h1>  
  
  <div class="controls">  
    <label>Expected IP Rating</label>  
    <input id="ip" type="text" placeholder="e.g. IP65" />  
  
    <label>Expected Form Rating</label>  
    <input id="form" type="text" placeholder="e.g. Form 4" />  
  
    <label>Expected Plinth Type</label>  
    <input id="plinth" type="text" placeholder="e.g. Concrete plinth" />  
  
    <label>Expected Material</label>  
    <input id="material" type="text" placeholder="e.g. Stainless Steel" />  
  
    <label>Upload Drawing PDF</label>  
    <input id="file" type="file" accept="application/pdf" />  
  
    <button onclick="checkPDF()">Check Drawing</button>  
  </div>  
  
  <canvas id="pdfCanvas"></canvas>  
  
  <div class="results" id="results"></div>  
  
  <script>  
    const canvas = document.getElementById('pdfCanvas');  
    const ctx = canvas.getContext('2d');  
  
    async function checkPDF() {  
      const file = document.getElementById('file').files[0];  
      if (!file) return alert('Please upload a PDF');  
  
      const expected = {  
        ip: document.getElementById('ip').value.toLowerCase(),  
        form: document.getElementById('form').value.toLowerCase(),  
        plinth: document.getElementById('plinth').value.toLowerCase(),  
        material: document.getElementById('material').value.toLowerCase(),  
      };  
  
      const pdfData = await file.arrayBuffer();  
      const pdf = await pdfjsLib.getDocument({ data: pdfData }).promise;  
      const page = await pdf.getPage(1);  
  
      const viewport = page.getViewport({ scale: 1.5 });  
      canvas.width = viewport.width;  
      canvas.height = viewport.height;  
      await page.render({ canvasContext: ctx, viewport }).promise;  
  
      let fullText = '';  
      const textContent = await page.getTextContent();  
      textContent.items.forEach(item => fullText += item.str + ' ');  
      fullText = fullText.toLowerCase();  
  
      const resultsDiv = document.getElementById('results');  
      resultsDiv.innerHTML = '<h3>Results</h3>';  
  
      Object.entries(expected).forEach(([key, value]) => {  
        if (!value) return;  
        const ok = fullText.includes(value);  
        const p = document.createElement('p');  
        p.textContent = `${key.toUpperCase()}: ${ok ? 'FOUND' : 'NOT FOUND'}`;  
        p.className = ok ? 'ok' : 'bad';  
        resultsDiv.appendChild(p);  
      });  
    }  
  </script>  
</body>  
</html>  
