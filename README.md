<!-- ===================================================================
     COVERAGE + BENEFITS SECTION  —  paste this ENTIRE block into one
     Elementor HTML widget. All CSS is scoped under #mntl-coverage so
     it will not affect the rest of your page (and won't collide with
     the #mntl-docs table — both can live on the same page).
     Edit names, plan details, and progress values directly below.
==================================================================== -->
<style>
#mntl-coverage *{box-sizing:border-box;margin:0;padding:0}
#mntl-coverage{
  --head:#15505f; --name:#16324a; --text:#2b3a4a; --muted:#6b7787;
  --card-1:#1b3a4f; --card-2:#0f2636;           /* dark insurance card gradient */
  --gray-bg:#e8eaed; --gray-tx:#45546a;
  --green-bg:#d4edd6; --green-tx:#37833f;
  --amber-tx:#bf7733;                            /* "% met" figure */
  --link:#2f8a99;
  --track:#e6e9ec; --fill:#16324a;               /* progress bar */
  --border:#eef0f2; --panel-bd:#e9edf0; --btn-bd:#d9dee3;
  font-family:"Figtree",-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
  color:var(--text);line-height:1.4;width:100%;-webkit-font-smoothing:antialiased;
}
#mntl-coverage .shadow{box-shadow:0 12px 34px -16px rgba(20,70,80,.30)}

/* ---------- top header bar ---------- */
#mntl-coverage .cov-bar{display:flex;align-items:center;gap:34px;flex-wrap:wrap;
  background:#fff;border:1px solid var(--panel-bd);border-radius:16px;padding:18px 24px;
  box-shadow:0 12px 34px -16px rgba(20,70,80,.30);margin-bottom:20px}
#mntl-coverage .who{display:flex;align-items:center;gap:14px}
#mntl-coverage .who .ring{flex:none;width:44px;height:44px;border-radius:50%;
  border:2px solid var(--gray-bg);display:flex;align-items:center;justify-content:center;color:var(--muted)}
#mntl-coverage .who .nm{font-size:17px;font-weight:700;color:var(--name);letter-spacing:-.2px}
#mntl-coverage .verified{display:inline-flex;align-items:center;gap:6px;margin-top:4px;
  background:var(--green-bg);color:var(--green-tx);font-size:12px;font-weight:600;
  padding:3px 10px;border-radius:20px}
#mntl-coverage .field .lab{font-size:11px;font-weight:600;letter-spacing:.6px;
  text-transform:uppercase;color:var(--muted);margin-bottom:4px}
#mntl-coverage .field .val{font-size:15px;font-weight:600;color:var(--name)}
#mntl-coverage .field .val .sub{color:var(--muted);font-weight:500;margin-left:8px}
#mntl-coverage .cov-bar .upd{margin-left:auto;display:inline-flex;align-items:center;gap:8px;
  border:none;cursor:pointer;background:var(--head);color:#fff;font-family:inherit;
  font-weight:600;font-size:14px;padding:11px 20px;border-radius:10px;transition:background .15s}
#mntl-coverage .cov-bar .upd:hover{background:#11414e}

/* ---------- two-column layout ---------- */
#mntl-coverage .cov-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;align-items:start}
#mntl-coverage .panel{background:#fff;border:1px solid var(--panel-bd);border-radius:16px;
  padding:22px 24px;box-shadow:0 12px 34px -16px rgba(20,70,80,.30)}
#mntl-coverage .panel > h4{font-size:15px;font-weight:700;color:var(--name);
  letter-spacing:-.1px;margin-bottom:16px}

/* ---------- insurance card ---------- */
#mntl-coverage .icard{position:relative;overflow:hidden;border-radius:14px;
  background:#fff;border:1px solid var(--panel-bd)}
#mntl-coverage .icard .ihead{position:relative;display:flex;align-items:flex-start;justify-content:space-between;
  background:linear-gradient(135deg,var(--card-1),var(--card-2));color:#fff;padding:18px 22px}
#mntl-coverage .icard .brand{font-size:19px;font-weight:700;letter-spacing:.2px}
#mntl-coverage .icard .tier{font-size:13px;font-weight:600;color:rgba(255,255,255,.85);
  border:1px solid rgba(255,255,255,.28);padding:3px 11px;border-radius:7px}
#mntl-coverage .icard .dots{position:absolute;top:12px;left:50%;transform:translateX(-50%);
  display:flex;gap:6px}
#mntl-coverage .icard .dots i{width:5px;height:5px;border-radius:50%;background:rgba(255,255,255,.22)}
#mntl-coverage .icard .ibody{padding:22px}
#mntl-coverage .icard .cgrid{display:grid;grid-template-columns:1fr 1fr;gap:18px 16px}
#mntl-coverage .icard .ci .k{font-size:11px;font-weight:600;letter-spacing:.5px;
  text-transform:uppercase;color:var(--muted);margin-bottom:5px}
#mntl-coverage .icard .ci .v{font-size:15px;font-weight:600;color:var(--name)}
#mntl-coverage .viewfull{display:inline-flex;align-items:center;gap:7px;margin-top:18px;
  width:100%;justify-content:center;color:var(--link);font-size:14px;font-weight:600;
  text-decoration:none}
#mntl-coverage .viewfull:hover{text-decoration:underline}

/* ---------- benefits ---------- */
#mntl-coverage .ben{padding:16px 0;border-bottom:1px solid var(--border)}
#mntl-coverage .ben:first-of-type{padding-top:0}
#mntl-coverage .ben:last-child{border-bottom:none;padding-bottom:0}
#mntl-coverage .ben .top{display:flex;align-items:baseline;justify-content:space-between;gap:12px}
#mntl-coverage .ben .blab{font-size:15px;font-weight:600;color:var(--name)}
#mntl-coverage .ben .met{font-size:14px;font-weight:700;color:var(--amber-tx);white-space:nowrap}
#mntl-coverage .ben .amt{font-size:13px;color:var(--muted);margin-top:3px}
#mntl-coverage .bar{height:9px;border-radius:6px;background:var(--track);margin-top:11px;overflow:hidden}
#mntl-coverage .bar > span{display:block;height:100%;border-radius:6px;background:var(--fill)}
#mntl-coverage .ben.pa .top{align-items:center}
#mntl-coverage .ben.pa .pmeta .amt{margin-top:2px}
#mntl-coverage .ben.pa .check{flex:none;width:34px;height:34px;border-radius:50%;
  background:var(--green-bg);color:var(--green-tx);display:flex;align-items:center;justify-content:center}

/* ---------- responsive ---------- */
@media(max-width:820px){
  #mntl-coverage .cov-grid{grid-template-columns:1fr}
}
@media(max-width:600px){
  #mntl-coverage .cov-bar{gap:18px 26px;padding:16px 18px}
  #mntl-coverage .cov-bar .upd{margin-left:0;width:100%;justify-content:center}
  #mntl-coverage .panel{padding:18px}
}
</style>

<div id="mntl-coverage">

  <!-- ===== header bar ===== -->
  <div class="cov-bar">
    <div class="who">
      <span class="ring">
        <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-6 8-6s8 2 8 6"/></svg>
      </span>
      <div>
        <div class="nm">Catherine</div>
        <span class="verified">
          <svg viewBox="0 0 24 24" width="13" height="13" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>
          Coverage verified
        </span>
      </div>
    </div>

    <div class="field">
      <div class="lab">Insurer</div>
      <div class="val">Blue Horizon Health <span class="sub">Blue Horizon PPO</span></div>
    </div>

    <div class="field">
      <div class="lab">Member ID</div>
      <div class="val">&bull;&bull;&bull;&bull; 4821</div>
    </div>

    <button class="upd">
      <svg viewBox="0 0 24 24" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4v6h6"/><path d="M20 20v-6h-6"/><path d="M5.5 9a8 8 0 0 1 13-2.5L20 8M18.5 15a8 8 0 0 1-13 2.5L4 16"/></svg>
      Update
    </button>
  </div>

  <!-- ===== two columns ===== -->
  <div class="cov-grid">

    <!-- insurance card -->
    <div class="panel">
      <h4>Insurance card</h4>

      <div class="icard">
        <div class="ihead">
          <span class="dots"><i></i><i></i><i></i></span>
          <span class="brand">Blue Horizon</span>
          <span class="tier">PPO</span>
        </div>
        <div class="ibody">
          <div class="cgrid">
            <div class="ci"><div class="k">Member Name</div><div class="v">Catherine</div></div>
            <div class="ci"><div class="k">Plan</div><div class="v">Blue Horizon PPO</div></div>
            <div class="ci"><div class="k">Member ID</div><div class="v">&bull;&bull;&bull;&bull; 4821</div></div>
            <div class="ci"><div class="k">Effective Date</div><div class="v">Jan 1, 2025</div></div>
            <div class="ci"><div class="k">Group Number</div><div class="v">7654</div></div>
          </div>
        </div>
      </div>

      <a class="viewfull" href="#">
        View full card
        <svg viewBox="0 0 24 24" width="15" height="15" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"><path d="M14 4h6v6"/><path d="M20 4l-9 9"/><path d="M19 14v5a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1h5"/></svg>
      </a>
    </div>

    <!-- benefits -->
    <div class="panel">
      <h4>Benefits</h4>

      <div class="ben">
        <div class="top">
          <span class="blab">Deductible progress</span>
          <span class="met">17% met</span>
        </div>
        <div class="amt">$250 of $1,500</div>
        <div class="bar"><span style="width:17%"></span></div>
      </div>

      <div class="ben">
        <div class="top">
          <span class="blab">Out-of-pocket progress</span>
          <span class="met">28% met</span>
        </div>
        <div class="amt">$850 of $3,000</div>
        <div class="bar"><span style="width:28%"></span></div>
      </div>

      <div class="ben pa">
        <div class="top">
          <div class="pmeta">
            <span class="blab">Prior authorization</span>
            <div class="amt">Not required</div>
          </div>
          <span class="check">
            <svg viewBox="0 0 24 24" width="17" height="17" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>
          </span>
        </div>
      </div>

    </div>

  </div>
</div>
