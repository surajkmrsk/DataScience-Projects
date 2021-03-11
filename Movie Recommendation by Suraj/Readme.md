***Movie Recommendation system***

We now live in what some call the “era of abundance”. For any given product, there are sometimes thousands of options to choose from. Think of the examples above: streaming videos, social networking, online shopping; the list goes on. Recommender systems help to personalize a platform and help the user find something they like.
The easiest and simplest way to do this is to recommend the most popular items. However, to really enhance the user experience through personalized recommendations, we need dedicated recommender systems.
From a business standpoint, the more relevant products a user finds on the platform, the higher their engagement. This often results in increased revenue for the platform itself. Various sources say that as much as 35–40% of tech giants’ revenue comes from recommendations alone.
Now that we understand the importance of recommender systems, let’s have a look at types of recommendation systems, then build our own with open-sourced data!

**Types of Recommender Systems**
Machine learning algorithms in recommender systems typically fit into two categories: content-based systems and collaborative filtering systems. Modern recommender systems combine both approaches.
Let’s have a look at how they work using movie recommendation systems as a base.
A) **Content-Based Movie Recommendation Systems**
Content-based methods are based on the similarity of movie attributes. Using this type of recommender system, if a user watches one movie, similar movies are recommended. For example, if a user watches a comedy movie starring Adam Sandler, the system will recommend them movies in the same genre or starring the same actor, or both. With this in mind, the input for building a content-based recommender system is movie attributes.
![image](https://user-images.githubusercontent.com/61193816/110740216-b1ffdb00-8258-11eb-9b5f-651d5ca9801e.png)

B) **Collaborative Filtering Movie Recommendation Systems**
With collaborative filtering, the system is based on past interactions between users and movies. With this in mind, the input for a collaborative filtering system is made up of past data of user interactions with the movies they watch.
For example, if user A watches M1, M2, and M3, and user B watches M1, M3, M4, we recommend M1 and M3 to a similar user C. You can see how this looks in the figure below for clearer reference.
![image](https://user-images.githubusercontent.com/61193816/110740249-c3e17e00-8258-11eb-862d-c0ebdcd851a1.png)

**The Dataset**
You can see a snapshot of the data below:
![image](https://user-images.githubusercontent.com/61193816/110740564-466a3d80-8259-11eb-95bb-8771d1aa8985.png)

**Implementation**
For our recommender system, we’ll use both of the techniques mentioned above: content-based and collaborative filtering. To find the similarity between movies for our content based method, we’ll use a cosine similarity function. For our collaborative filtering method, we’ll use a matrix factorization technique.
The first step towards this is creating a matrix factorization based model. We’ll use the output of this model and a few handcrafted features to provide inputs to the final model. The basic process will look like this:
Step 1: Build a matrix factorization-based model
Step 2: Create handcrafted features
