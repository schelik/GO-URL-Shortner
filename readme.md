# URL Shortner
<p>Created url shortner APIs using Golang, Gin & Redis. It also returns the original long url if the short url is provided.</p>
<p>Frameworks/Libraries: Golang, Redis, Docker<br />
Tools/Technologies: Gin, SHA256, Base58</p>

<h2>Implementation</h2>
<li>The mapping between the original Url and the generated short Url is stored in Redis</li>
<li>Test files consist of unit and integration tests for the database and GenerateShortLink method</li>
<li>Hashing the long url + userId with SHA256. The userId is added to prevent providing same urls to different users in case they want to shorten the same link.</li>
<li>Derive a big integer number from the hash bytes generated during the hasing</li>
<li>Lastly apply Base58 on the derived big integer value and pick the first 8 characters</li>
<li>Dockerized the web app and uploaded the docker image to AWS platform</li>


<h2>Time & Effort</h2>
The project took ~20 hours in total, within 5 days.
