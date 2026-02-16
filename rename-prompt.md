You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Systems Group Of Companies | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Systems Group Of Companies | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/6d95c421cfdc25743ca3bee482775041.css",
    "context": {
      "path": "css/6d95c421cfdc25743ca3bee482775041.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css",
    "context": {
      "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/169caa2505416001e404acc3529049fd.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/2216ee1a2accb36f4dad730df26d11a0.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2400b0f3960c118ec3b8532513a52ef2.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d28a68166f6bc7533e2eb12c4c73ddf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3749483819a7902ce54acc2487bd4e5a.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3758ca0cc1cbaa8933fba58c0ada84a1.webp",
    "context": {
      "refs": [
        {
          "alt": "PoolMaintenance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3bb64de4ad02ffb9df6adbf9173f3320.webp",
    "context": {
      "refs": [
        {
          "alt": "CateringServices",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c4e68880b59e4381964194da03031f5.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20210503at12647PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e789dc3c9a6a91e96cbea1599302b4f.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR MISSION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/420b6c51563c5486bea20da2723609d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/538b5f91b3f8635304d49ccb204ea6ae.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR PEOPLE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6db2f5265f33c26fbbb16d2c0b0f7878.webp",
    "context": {
      "refs": [
        {
          "alt": "shutterstock",
          "title": ""
        },
        {
          "alt": "shutterstock",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70c53b04cd8b56dff24acc2a4654d3ce.webp",
    "context": {
      "refs": [
        {
          "alt": "ElectricalMaintenance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76e5940bdeac507c1cab86391c941c86.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ee7c1eebd0abc554f1c58fbe6d9a192.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20210503at12647PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/842cf74bbd9c6699f1e33ced903cfc5a.webp",
    "context": {
      "refs": [
        {
          "alt": "Bedbugs",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/999f76461f0a318d5b42ddf59d69fab8.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f13db2c762dc91d3de6f4fa9ef3b236.webp",
    "context": {
      "refs": [
        {
          "alt": "HouseKeeping",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0cf2ddbcfe6cce741b44241f508f9db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1f6b61b88708f90ab63a4feb49fb962.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aaa082c69a3582428998ab5b3211ddfa.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1e91bdf49c439da51503c9946c866cf.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20210503at12646PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5c71cc16d7495d83c6206fb2126f234.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR VALUES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb53293e1d82126e40df81a8ecd4d43a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f216aa61a802854f22119cd52cc92967.webp",
    "context": {
      "refs": [
        {
          "alt": "GardenMaintenance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa47c644b7dc1e5cf87ac5c7d4ab8c91.webp",
    "context": {
      "refs": [
        {
          "alt": "istockphoto1185738880612x612",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Systems Group Of Companies | Home",
      "first_heading": "Systems Pest Management Services Pvt LtdSysman Facility Management Services Pvt Ltd"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "Systems Group Of Companies | Services",
      "first_heading": "SERVICES"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.