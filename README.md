<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Limraz Luxe Salon WhatsApp Widget</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=Jost:wght@300;400;500&display=swap');
        
        * { 
            box-sizing: border-box; 
            margin: 0; 
            padding: 0; 
        }

        .lw { 
            font-family: 'Jost', sans-serif; 
            padding: 1.5rem 0; 
            background-color: #f5f5f5; /* Added background for visibility */
        }

        .lw-card {
            background: #0a0a0a;
            border-radius: 16px;
            max-width: 500px;
            margin: 0 auto;
            overflow: hidden;
            border: 0.5px solid #2a2a2a;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .lw-hero {
            padding: 2rem 2rem 1.5rem;
            border-bottom: 0.5px solid #1e1e1e;
            text-align: center;
        }

        .lw-logo-wrap {
            background: #000;
            border-radius: 10px;
            padding: 1rem 1.5rem 0.75rem;
            display: inline-block;
            margin-bottom: 1.2rem;
            border: 0.5px solid #222;
        }

        .lw-brand { font-family: 'Cormorant Garamond', serif; }

        .lw-brand-main {
            font-size: 32px; 
            font-weight: 600; 
            letter-spacing: 10px;
            color: #fff; 
            display: block; 
            line-height: 1;
        }

        .lw-brand-main span { color: #c9a84c; }

        .lw-brand-sub {
            font-size: 11px; 
            font-weight: 300; 
            letter-spacing: 6px;
            color: #c9a84c; 
            display: block; 
            margin-top: 6px;
            text-transform: uppercase;
        }

        .lw-tagline {
            font-size: 13px; 
            color: #888; 
            font-weight: 300;
            letter-spacing: 0.04em; 
            line-height: 1.6;
        }

        .lw-tagline strong { color: #c9a84c; font-weight: 400; }

        .lw-services {
            padding: 1.25rem 2rem;
            border-bottom: 0.5px solid #1e1e1e;
        }

        .lw-services-label {
            font-size: 10px; 
            letter-spacing: 3px; 
            color: #555;
            text-transform: uppercase; 
            margin-bottom: 10px;
        }

        .lw-chips { 
            display: flex; 
            flex-wrap: wrap; 
            gap: 7px; 
        }

        .lw-chip {
            background: #141414;
            border: 0.5px solid #2a2a2a;
            border-radius: 100px;
            font-size: 12px; 
            color: #bbb;
            padding: 5px 13px; 
            cursor: pointer;
            transition: all 0.18s; 
            font-weight: 300;
        }

        .lw-chip:hover, .lw-chip.active {
            border-color: #c9a84c;
            color: #c9a84c;
            background: #1a1507;
        }

        .lw-msg-preview {
            margin: 1rem 2rem;
            background: #111;
            border-radius: 10px;
            border: 0.5px solid #222;
            padding: 10px 14px;
            font-size: 12px; 
            color: #777;
            transition: all 0.2s;
            min-height: 42px;
            display: flex; 
            align-items: center; 
            gap: 8px;
        }

        .lw-msg-preview .dot {
            width: 6px; 
            height: 6px; 
            border-radius: 50%;
            background: #c9a84c; 
            flex-shrink: 0;
        }

        .lw-msg-text { 
            color: #aaa; 
            font-style: italic; 
            line-height: 1.5; 
        }

        .lw-bottom { padding: 0 2rem 1.75rem; }

        .lw-cta {
            display: flex; 
            align-items: center; 
            justify-content: center; 
            gap: 10px;
            background: #25d366;
            color: #fff; 
            font-family: 'Jost', sans-serif;
            font-size: 14px; 
            font-weight: 500; 
            letter-spacing: 0.5px;
            border: none; 
            border-radius: 10px;
            padding: 14px 24px; 
            width: 100%;
            cursor: pointer; 
            text-decoration: none;
            transition: background 0.18s, transform 0.1s;
        }

        .lw-cta:hover { background: #1ebe5c; }

        .lw-cta:active { transform: scale(0.98); }

        .lw-note {
            text-align: center; 
            font-size: 11px;
            color: #444; 
            margin-top: 10px; 
            letter-spacing: 0.03em;
        }

        .lw-note span { color: #c9a84c; }
    </style>
</head>
<body>

<div class="lw">
  <div class="lw-card">
    <div class="lw-hero">
      <div class="lw-logo-wrap">
        <div class="lw-brand">
          <span class="lw-brand-main">LI<span>M</span>RAZ</span>
          <span class="lw-brand-sub">Luxe' Salon</span>
        </div>
      </div>
      <p class="lw-tagline">
        Where every visit is a <strong>luxury experience</strong>.<br>
        Book your appointment in seconds — just tap below.
      </p>
    </div>

    <div class="lw-services">
      <p class="lw-services-label">What can we help you with?</p>
      <div class="lw-chips">
        <span class="lw-chip" onclick="selectService(this, 'Book an Appointment')">Book Appointment</span>
        <span class="lw-chip" onclick="selectService(this, 'Hair Services')">Hair Services</span>
        <span class="lw-chip" onclick="selectService(this, 'Skin & Facial')">Skin & Facial</span>
        <span class="lw-chip" onclick="selectService(this, 'Bridal Package')">Bridal Package</span>
        <span class="lw-chip" onclick="selectService(this, 'Nail Art')">Nail Art</span>
        <span class="lw-chip" onclick="selectService(this, 'Service Enquiry')">Service Enquiry</span>
      </div>
    </div>

    <div class="lw-msg-preview" id="msgPreview">
      <div class="dot"></div>
      <span class="lw-msg-text" id="msgText">Tap a service above to personalise your message →</span>
    </div>

    <div class="lw-bottom">
      <a class="lw-cta" id="waLink" href="https://wa.me/916380634564?text=Hi%20Limraz%20Luxe%27%20Salon%2C%20I%20would%20like%20to%20enquire%20about%20your%20services." target="_blank">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
        Chat on WhatsApp
      </a>
      <p class="lw-note">+91 63806 34564 &nbsp;·&nbsp; <span>We reply within minutes</span></p>
    </div>
  </div>
</div>

<script>
    const messages = {
      'Book an Appointment': "Hi Limraz Luxe' Salon! I'd like to book an appointment. Please share available slots.",
      'Hair Services': "Hi Limraz Luxe' Salon! I'm interested in your Hair Services. Can you share details & pricing?",
      'Skin & Facial': "Hi Limraz Luxe' Salon! I'd like to know more about your Skin & Facial treatments.",
      'Bridal Package': "Hi Limraz Luxe' Salon! I'm looking for a Bridal Package. Can you help me with options?",
      'Nail Art': "Hi Limraz Luxe' Salon! I'm interested in your Nail Art services. What designs do you offer?",
      'Service Enquiry': "Hi Limraz Luxe' Salon! I'd like to enquire about your services and pricing."
    };

    function selectService(el, service) {
      // Remove active class from all chips
      document.querySelectorAll('.lw-chip').forEach(c => c.classList.remove('active'));
      // Add active class to clicked chip
      el.classList.add('active');
      
      const msg = messages[service];
      // Update preview text
      document.getElementById('msgText').textContent = '"' + msg + '"';
      // Update WhatsApp URL
      document.getElementById('waLink').href = 'https://wa.me/916380634564?text=' + encodeURIComponent(msg);
    }
</script>

</body>
</html>
