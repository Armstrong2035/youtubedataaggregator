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
I will use React for this project, and the pseudo code is as follows: 
``` Pseudo
App() { 
state variable that holds the API key

return <>
    <Search {api key passed as prop} />
        </>
}

Search({receive api key as prop}) {

[query, setQuery] = useState('')

receiveQuery{
    event handler callback that tracks keystroke, and updates form accordingly.
    if (input is a url){
    channelId = 
        First handle error to ensure that it is a YouTube link.
        Then collect the channel Id that appears in the url.
setQuery(channelid)
        }
    if (input is not a url) {
setQuery(channelName)
    
}
}

return <>
    <form {setQuery when form is filled}> Paste Youtube channel link, or type the username </form>
    <ApiCall {api key passed as prop}, {query passed as prop} />
}


ApiCall({receive api key as prop, received query as prop}){
[metaData, setMetaData] = useState[]
use api key and query to find, and view the youtube channel information.
Then pasrse it into Json and setMetaData

return <>
    <ChannelPopularity {send meta data as prop} />
    <ChannelEngagement {send meta data as prop} />
    <ChannelActivity {send meta data as prop} />
        </>
}

ChannelPopularity(metaData) {
retrieve and display relevant data
}

ChannelEngagement(metaData) {
retrieve and display relevant data
}

ChannelActivity(metaData) {
retrieve and display relevant data
}




```

### Calculating and displaying the data: 
I presume that the bulk of the data will be shown as is, but not all. The ones I believe should be calculated are as follows: 

- Most Popular videos (Top 10 videos will be shown. unlock more in  a premium plan)
    - Engagement rate per video
    - Popular keywords and tags. (this would require collecting the keywords from most popular videos and analysing them with a LLM like ChatGPT to provide some context.
    - Average Video Duration
    - Time of day analysis
    - Comparative analysis with channels in the same category
    - Video performance by category



  
      
