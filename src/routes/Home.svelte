<script>
  import NavigationBar from "../components/NavigationBar.svelte";
  export let imageSrc = "nidhi.jpg";
  let about =
    "This was the most difficult question for me to answer in any interview because I don't think any one can answer this question in a true manner. Because a person can't know herself completely. Truly speaking, I have outperformed at things I thought I would really suck at!! For example, I never cooked in my life and I thought I would be the worst cook ever, if and when I did cook, but once I got myself into it I actually was better than I expected myself to be, so much so that I have my own food blog! The only thing I have learnt is to not say No to learning and experimenting. I did my bachelors in IT field but when given an opportunity to learn finance during MBA, I took that chance and did fine. Later I got an opportunity to work as an freelance HR professional, which I did with complete honesty. I did that for 3 months. Things I learnt is that your hard work, dedication and consistent effort always pays. I am a person likes to do her job better than she did yesterday. I like to evolve by means of constant learning, changing my ways when its required (and even my field as a matter of fact), and by being aware of what I don't know. I firmly believe that every human has the capacity to be great. Its our own inhibitions that stops our growth. the only thing I want to achieve is that I grow to the fullest of my capacity.";
  let sub =
    " A Mom | A Homemaker | A Cook | A Writer | A Dancer | A Freelancer | PGDM in Finance | Bachelors in Information Technology  ";
</script>

<!-- <style type="text/css">
  @import "../styles/HomeStyle.css";
</style> -->

<svelte:head>
  <title>Home</title>
</svelte:head>
<body>

  <div class="aboutMeSection">
    <h2 class="aboutMeHead">About Me</h2>
    <div class="imageContainer">
      <img class="NidhiImage" src={imageSrc} alt="About Nidhi" />
    </div>
    <div class="aboutMeText">
      <h3 class="subHead">Nidhi Sharma</h3>
      <h5 class="subText">{sub}</h5>
      {about}
    </div>
  </div>
</body>
