---
layout: base
title: Tutoring · Nellie Kolon
description: SAT prep, AP Biology, and AP Chemistry tutoring with Nellie Kolon, in person in Atlanta or online.
image: /assets/media/headshot.jpg
permalink: /tutoring/
---

<section class="intro">
  <div class="intro-text">
    <h1>Tutoring</h1>
    <p class="role">SAT prep, AP Biology, and AP Chemistry</p>
    <p class="lede">I’m a biochemist and biomedical engineer, and I’ve been tutoring high school students since 2022. I love helping students understand why the science works, not just memorize it, and building the test strategies that make SAT day less stressful.</p>
    <div class="links">
      <a class="button primary" href="#request">Request tutoring</a>
    </div>
  </div>
  <img class="headshot" src="/assets/media/headshot.jpg" alt="Portrait of Nellie Kolon">
</section>

<section id="offer">
  <div class="section-head">
    <p class="eyebrow">What I offer</p>
    <h2>Subjects and sessions</h2>
  </div>
  <div class="offer-grid">
    <div class="offer">
      <h3>SAT prep</h3>
      <p>Math and reading practice, test strategy, and timed practice sections.</p>
    </div>
    <div class="offer">
      <h3>AP Biology</h3>
      <p>Concept review, lab and data questions, and exam prep.</p>
    </div>
    <div class="offer">
      <h3>AP Chemistry</h3>
      <p>Problem solving, calculations, and exam prep.</p>
    </div>
  </div>
  <ul class="points">
    <li>In person in Atlanta, or online over video</li>
    <li>Flexible scheduling, including evenings and weekends</li>
  </ul>
</section>

<section id="request">
  <div class="section-head">
    <p class="eyebrow">Get started</p>
    <h2>Request tutoring</h2>
    <p class="meta">I’ll reply by email within two days.</p>
  </div>
  <form class="tutor-form" id="tutor-form" action="https://formspree.io/f/FORM_ID" method="POST">
    <div class="field">
      <label for="name">Your name</label>
      <input id="name" name="name" type="text" autocomplete="name" required>
    </div>
    <div class="field-row">
      <div class="field">
        <label for="email">Email</label>
        <input id="email" name="email" type="email" autocomplete="email" required>
      </div>
      <div class="field">
        <label for="phone">Phone <span class="optional">(optional)</span></label>
        <input id="phone" name="phone" type="tel" autocomplete="tel">
      </div>
    </div>
    <div class="field">
      <label for="relationship">I am a</label>
      <select id="relationship" name="relationship" required>
        <option value="">Choose one</option>
        <option>Parent or guardian</option>
        <option>Student</option>
      </select>
    </div>
    <div class="field">
      <label for="grade">Student’s grade</label>
      <select id="grade" name="grade" required>
        <option value="">Choose one</option>
        <option>9th</option>
        <option>10th</option>
        <option>11th</option>
        <option>12th</option>
        <option>Other</option>
      </select>
    </div>
    <fieldset class="field">
      <legend>Subjects</legend>
      <label class="check"><input type="checkbox" name="subjects" value="SAT prep" id="subj-sat"> SAT prep</label>
      <label class="check"><input type="checkbox" name="subjects" value="AP Biology" id="subj-bio"> AP Biology</label>
      <label class="check"><input type="checkbox" name="subjects" value="AP Chemistry" id="subj-chem"> AP Chemistry</label>
    </fieldset>
    <fieldset class="field">
      <legend>Format</legend>
      <label class="check"><input type="radio" name="format" value="In person" id="fmt-in" required> In person</label>
      <label class="check"><input type="radio" name="format" value="Online" id="fmt-online"> Online</label>
      <label class="check"><input type="radio" name="format" value="Either" id="fmt-either"> Either</label>
    </fieldset>
    <div class="field">
      <label for="availability">When are you usually available?</label>
      <input id="availability" name="availability" type="text" placeholder="For example, weekday evenings or Sunday mornings">
    </div>
    <div class="field">
      <label for="message">Anything else I should know? <span class="optional">(optional)</span></label>
      <textarea id="message" name="message" rows="4" placeholder="Goals, test dates, or what’s been hard so far"></textarea>
    </div>
    <input type="text" name="_gotcha" class="hp" tabindex="-1" autocomplete="off" aria-hidden="true">
    <button class="button primary" type="submit">Send request</button>
    <p class="form-status" id="form-status" role="status"></p>
  </form>
</section>

<script>
  (function () {
    var form = document.getElementById('tutor-form');
    var status = document.getElementById('form-status');
    if (!form || !window.fetch) return;
    form.addEventListener('submit', function (e) {
      e.preventDefault();
      var subjects = form.querySelectorAll('input[name="subjects"]:checked');
      if (subjects.length === 0) {
        status.textContent = 'Please choose at least one subject.';
        return;
      }
      status.textContent = 'Sending…';
      fetch(form.action, { method: 'POST', body: new FormData(form), headers: { 'Accept': 'application/json' } })
        .then(function (r) {
          if (r.ok) {
            form.reset();
            status.textContent = 'Thanks! Your request was sent. I’ll reply by email within two days.';
          } else {
            status.textContent = 'Something went wrong sending your request. Please email me at nellie@kolon.org.';
          }
        })
        .catch(function () {
          status.textContent = 'Something went wrong sending your request. Please email me at nellie@kolon.org.';
        });
    });
  })();
</script>
