<script>
    const regex = /([\n\s]+)/gm;

    let valueUserFriendly = "";
    $: valueCiFriendly = valueUserFriendly
        .replace("\"", "\\\"")
        .replace(regex, "");
</script>

<main>
    <h1>Bitrise CI API Helper</h1>
    <p>User Friendly</p>
    <textarea bind:value={valueUserFriendly} name="Text1" cols="40" rows="5"></textarea>
    <p>CI Friendly</p>
    <textarea bind:value={valueCiFriendly} name="Text1" cols="40" rows="5"></textarea>
</main>