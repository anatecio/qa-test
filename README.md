# Exercice 1 - Test Plan

The goal is to write a test plan, in **french**.

In case you find elements that are not clear / specified enough, you will need to make (reasonable) choices and note them.

The handling of `images_url` is optionnal (do the rest first).


## API OVERVIEW

Here is a (very short) description of the api.

### 1/ configuration endpoint

> GET api/users/:user_id


### 2/ listing of created adverts

> GET api/users/:user_id/adverts

```
An example of result:
{
  adverts: [
    {
      id: 1,
      seller_id: 2,
      description: "buy my car, it looks old but it is solid',
      price: 3000,
      creation_date: "2020-01-01",
      images_url: [
        'https://some_image_1',
        'https://some_image_2'
      ]
    }
  ]
}
```

## 3/ create an advert

> POST api/users/:user_id/adverts

returns:
- 200: the created advert is returned
- 422: a payload is returned, here is an example:
```
{
    errors: [
      {
        message: 'some reason',
        details: {}
    ]
}
```

## HOW IT WORKS

Somebody said that our API allows users to create adverts.
A user can create an advert if:
- user_status is 'paid' or 'demo'
- quota is not 0
- the content is complete and coherent


# Exercice 2 - Functional API Testing

Functional automation for API testing. Write a test in your `$favorite_language` for the following REST API:

https://jsonplaceholder.typicode.com/

Requirements:
- Get a random user (userID), print out its email address to console.
- Using this userID, get this user’s associated posts and verify they contains a valid Post IDs (an Integer between 1 and 100).
- Do a post using same userID with a non-empty title and body, verify the correct response is returned (since this is a mock API, it might not return Response code 200, so check the documentation).



# Acknowledgement

Inspired heavily by https://github.com/gumtreeuk.
