---
title: "July 5 – July 11"
date: 2026-07-05
hide_from_progress_index: true
tags:
  - progress-week
diff_geo_entries:
  - date: "7/5/26"
    summary:
      "Started reading proof of Proposition 3, skimmed the torus example, and
      spent about 30 minutes."
    images:
      - "/img/progress/2026-w28/math7-5-26-p1.jpg"
      - "/img/progress/2026-w28/math7-5-26-p2.jpg"
---

<div class="week">
  <h2>Week of July 5 – July 11</h2>
  <table class="progress-table">
    <thead>
      <tr>
        <th>Item</th>
        <th data-date="7/5">Sun<br>7/5</th>
        <th data-date="7/6">Mon<br>7/6</th>
        <th data-date="7/7">Tue<br>7/7</th>
        <th data-date="7/8">Wed<br>7/8</th>
        <th data-date="7/9">Thu<br>7/9</th>
        <th data-date="7/10">Fri<br>7/10</th>
        <th data-date="7/11">Sat<br>7/11</th>
      </tr>
    </thead>
    <tbody>
      <tr data-item="agt"><th>AGT</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
      <tr data-item="diff-geo"><th>Diff geo</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
      <tr data-item="combinatorics"><th>Combinatorics</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
      <tr data-item="mechanics"><th>Mechanics</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
      <tr data-item="ml"><th>ML</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
      <tr data-item="app"><th>App</th><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
    </tbody>
  </table>

  <div class="day-log" data-date="7/7">
    <h3>Tue 7/7</h3>
    Nothing. Played One Piece. Knew I was going to play, so tried reading ML at work, but was also unusually tired at work.
  </div>

  <div class="day-log" data-date="7/6">
    <h3>Mon 7/6</h3>
    The animation still has a 75% skip rate off of 150 or so views. It's just a loop of one second, so something needs to happen in the 2nd second.
    <ul>
      <li data-item="mechanics">Skimmed the linear algebra stuff (up to 1.5 yeah not a lot).</li>
      <li data-item="combinatorics">Read a few examples of pigeonhole and did the first 3 "check yourself" exercises. Stopped before the generalized pigeonhole principle.</li>
    </ul>
  </div>

  <div class="day-log" data-date="7/5">
    <h3>Sun 7/5</h3>
    Textbooks for mechanics and combinatorics coming in mail tomorrow.
    <ul>
      <li data-item="agt">Finished hunter gif and percy gag.</li>
      <li data-item="app"><a href="{{ site.baseurl }}/apps/webtoon-stitcher#75226">Webtoon Stitcher — marker lines feature</a></li>
      <li data-item="diff-geo">Differential geometry: started reading proof of Proposition 3, skimmed torus example (~30 min).</li>
      <li data-item="ml">ML: started reading <a href="https://jax-ml.github.io/scaling-book/">How To Scale Your Model</a>, prerequisites — <a href="https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/">Jay Alammar on seq2seq attention</a></li>
    </ul>
    <div style="display: flex; gap: 10px; flex-wrap: wrap;">
      <img src="{{ site.baseurl }}/img/progress/2026-w28/math7-5-26-p1.jpg" alt="Differential geometry notes, page 1" style="flex: 1; min-width: 200px; width: 0; height: auto;">
      <img src="{{ site.baseurl }}/img/progress/2026-w28/math7-5-26-p2.jpg" alt="Differential geometry notes, page 2" style="flex: 1; min-width: 200px; width: 0; height: auto;">
    </div>
    <img src="{{ site.baseurl }}/img/progress/2026-w28/hunter-bandage-2.gif" alt="Hunter bandage gif" style="width: 200px; max-width: 100%; height: auto;">
  </div>
</div>

<style>
.progress-table {
  border-collapse: collapse;
  width: 100%;
  margin: 15px 0;
  text-align: center;
}
.progress-table th,
.progress-table td {
  border: 1px solid #ddd;
  padding: 8px 6px;
}
.progress-table thead th {
  background: #f5f5f5;
  font-weight: 600;
  font-size: 0.9em;
}
.progress-table tbody th {
  text-align: left;
  background: #fafafa;
  white-space: nowrap;
}
.progress-table td {
  color: #2e7d32;
  font-weight: 700;
}
.day-log {
  margin: 20px 0 40px 0;
}
.day-log h3 {
  margin-bottom: 5px;
}
</style>

<script>
document.querySelectorAll('.week').forEach(function (week) {
  var filled = {};
  week.querySelectorAll('.day-log').forEach(function (day) {
    var date = day.getAttribute('data-date');
    day.querySelectorAll('li[data-item]').forEach(function (li) {
      if (li.textContent.trim() !== '') {
        filled[li.getAttribute('data-item') + '|' + date] = true;
      }
    });
  });

  var table = week.querySelector('.progress-table');
  if (!table) return;

  var dates = [];
  table.querySelectorAll('thead th[data-date]').forEach(function (th) {
    dates.push(th.getAttribute('data-date'));
  });

  table.querySelectorAll('tbody tr[data-item]').forEach(function (row) {
    var item = row.getAttribute('data-item');
    var cells = row.querySelectorAll('td');
    dates.forEach(function (date, i) {
      if (cells[i] && filled[item + '|' + date]) {
        cells[i].textContent = '✓';
      }
    });
  });
});
</script>
