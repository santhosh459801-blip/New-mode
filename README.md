# New-mode:root{
  --bg:#f6f6f6;
  --card:#ffffff;
  --accent:#2f2f2f;
  --muted:#6b6b6b;
  --maxwidth:1000px;
  --gap:20px;
  --accent-2:#dcdcdc;
  font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
  color:var(--accent);
}

*{box-sizing:border-box}
body{
  margin:0;
  background:var(--bg);
  color:var(--accent);
  line-height:1.5;
  -webkit-font-smoothing:antialiased;
}

.hero{
  background:linear-gradient(90deg, rgba(255,255,255,0.9), rgba(245,245,245,0.9));
  border-bottom:1px solid var(--accent-2);
  padding:30px 16px;
}
.hero-inner{
  max-width:var(--maxwidth);
  margin:0 auto;
  display:flex;
  align-items:center;
  gap:16px;
}
.profile-photo{
  width:120px;
  height:120px;
  object-fit:cover;
  border-radius:8px;
  border:4px solid white;
  box-shadow:0 6px 18px rgba(0,0,0,0.08);
}
.hero-text h1{
  margin:0;
  letter-spacing:2px;
  font-size:28px;
}
.subtitle{
  margin:6px 0 8px;
  color:var(--muted);
}

.contact-inline{
  color:var(--muted);
  font-size:14px;
}
.contact-inline a{ color:inherit; text-decoration:none }

.container{
  max-width:var(--maxwidth);
  margin:28px auto;
  display:grid;
  grid-template-columns: 300px 1fr;
  gap:var(--gap);
  padding:0 16px 40px;
}

/* left column cards */
.left-column .card,
.right-column .card{
  background:var(--card);
  padding:18px;
  border-radius:10px;
  box-shadow:0 6px 18px rgba(0,0,0,0.04);
  margin-bottom:var(--gap);
}

.left-column h2,
.right-column h2{ margin-top:0; font-size:18px; letter-spacing:1px }

.left-column ul,
.right-column ul{ padding-left:18px; margin:8px 0; color:var(--muted) }

.right-column .card p{ color:var(--muted) }

.project h3{ margin:6px 0 2px; font-size:16px }

footer.footer{
  text-align:center;
  color:var(--muted);
  padding:18px 0 40px;
}

/* Responsive */
@media (max-width:880px){
  .container{ grid-template-columns: 1fr; }
  .hero-inner{ flex-direction:row; gap:12px; align-items:center }
  .profile-photo{ width:100px; height:100px }
}
@media (max-width:480px){
  .hero-inner{ flex-direction:column; align-items:center; text-align:center }
  .contact-inline{ display:block; margin-top:8px }
}
