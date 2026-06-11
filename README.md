# Love
Testing
<!DOCTYPE html>
<html>
<head>
    <style>
        .test-box {
            background-color: #ffe6e6;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            padding: 30px;
            border-radius: 20px;
            border: 3px dashed #ff7675;
            position: relative;
            max-width: 500px;
            margin: 20px auto;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .preview-tag {
            background: #ff7675;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 15px;
        }
        .test-gift {
            font-size: 50px;
            cursor: pointer;
            animation: testBounce 2s infinite;
            display: inline-block;
        }
        @keyframes testBounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-15px); }
        }
        .btn-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            height: 50px;
            position: relative;
        }
        .t-btn {
            padding: 10px 25px;
            font-size: 16px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.2s ease;
        }
        #tYes { background: #ff7675; color: white; }
        #tNo { background: #b2bec3; color: white; position: absolute; left: 55%; }
        .heart-f {
            position: absolute;
            color: #ff7675;
            opacity: 0.6;
            animation: fUp 4s linear infinite;
        }
        @keyframes fUp {
            0% { transform: translateY(150px) scale(0.5); opacity: 1; }
            100% { transform: translateY(-150px) scale(1.2); opacity: 0; }
        }
    </style>
</head>
<body>

<div class="test-box">
    <div class="preview-tag">LIVE TESTING WINDOW 🛠️</div>
    <h2 style="color: #d63031; margin-top: 0;">Happy Birthday, My Love! 💖</h2>
    
    <!-- Floating heart simulation -->
    <span class="heart-f" style="left: 20%; animation-delay: 0s;">❤️</span>
    <span class="heart-f" style="left: 80%; animation-delay: 2s;">❤️</span>

    <div class="test-gift" onclick="alert('🎶 *Romantic Music Playing...* \n(Jab aap file bnaoge toh asli gaana bajega!)')">🎁</div>
    <p style="font-size: 12px; color: #636e72;">^ Gift par click karke music test karo</p>

    <h3 style="color: #2d3436; margin-top: 20px;">Do you love me?</h3>
    
    <div class="btn-container" id="boxBounds">
        <button class="t-btn" id="tYes" onclick="alert('Yay! ❤️ I love you too!')">Yes!</button>
        <button class="t-btn" id="tNo" onmouseover="moveNo()" onclick="moveNo()">No</button>
    </div>
</div>

<script>
    function moveNo() {
        const btn = document.getElementById('tNo');
        // Box ke andar hi button ko random jagah bhagane ke liye code
        const x = Math.random() * 70 - 35; // Random X shift
        const y = Math.random() * 60 - 30; // Random Y shift
        
        btn.style.transform = `translate(${x}px, ${y}px)`;
    }
</script>

</body>
</html>
