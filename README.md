# YouTube Data Aggregator
Find statistics about any YouTube channel

## Introduction
This Readme will be updated as I continue. For now, it will serve as storage for my approach to solving this problem. 

### What kind of data do I want from the YouTube Data API?
The data when viewed as a unit should give insight into the relationship between the channel's activity, its engagement, and its popularity. This should help users discover patterns that they can replicate. 
- Channel popularity
    - Subscriber count
    - View count
    - Average view duration
- Channel engagement
    - Comments
    - Likes
    - Dislikes
    - Uploads
- Channel Activity
    - Uploads
        - Upload time
        - Video length
        - Upload frequency
    - Page SEO data
        - Channel category
        - Tags used in videos
        - Description in Videos
     
### How would I code this? 
I will use React for this project, and the component structure should be as follows: 
``` Pseudo
App() { 
state variable that holds the API key

return <>
    <Search {api key passed as prop} />
        </>
}

Search({receive api key as prop}) {

receiveQuery{
    event handler callback that tracks keystroke, and updates form accordingly.
    if (input is a url){
        First handle error to ensure that it is a YouTube link.
        Then collect the channel Id that appears in the url. 
        }
}

return <>
    <form> </form>
    <ApiCall {api key passed as prop} />
}


ApiCall({receive api key as prop}){
async API

}

```

  
      
