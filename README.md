<ul>
  <li>
    <span>콤부차</span>
    <button class="count-btn" data-count="1">+1</button>
    <button class="count-btn" data-count="2">+2</button>
    <span class="count">0</span>
  </li>
</ul>

<script>
  // 버튼 클릭 이벤트 처리
  const countBtns = document.querySelectorAll('.count-btn');
  const countSpans = document.querySelectorAll('.count');
  const productNames = document.querySelectorAll('li span');
  
  countBtns.forEach((btn, index) => {
    btn.addEventListener('click', () => {
      const count = parseInt(btn.getAttribute('data-count'));
      const currentCount = parseInt(countSpans[index].textContent);
      const newCount = currentCount + count;
      countSpans[index].textContent = newCount;
    });
  });
</script>
