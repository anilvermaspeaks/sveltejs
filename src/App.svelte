<script>
  import Header from "./UI/Header.svelte";
  import MeetupGrid from "./Meetups/MeetupGrid.svelte";
  let title = "hello";
  let meetups = [];

  let subtitle = "";
  let description = "";
  let email = "";
  const addAMeet = () => {
    const newMeetup = {
      id: Math.random().toString(),
      title,
      subtitle,
      description,
      email,
    };
    meetups = [...meetups, { ...newMeetup }];
    console.log(meetups);
  };
</script>

<main>
  <form class="meetupForm" on:submit|preventDefault={addAMeet}>
    <label>
      Title
      <input type="text" bind:value={title} placeholder="title" />
    </label>
    <label>
      Subtitle
      <input type="text" bind:value={subtitle} placeholder="subtitle" />
    </label>
    <label>
      Description
      <textarea bind:value={description} placeholder="description" />
    </label>
    <label>
      Description
      <input bind:value={email} type="email" placeholder="email" />
    </label>

    <label>
      <input type="submit" value="Add a Meet" />
    </label>
  </form>

  <Header />
  <MeetupGrid {meetups} />
</main>
