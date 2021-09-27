# TACO lab page

This is repository for [TACO lab page](https://taco-lab.net/). We use Jekyll to run our Github page. We are welcome for other people to contribute to our site not just lab members. Feel free to fork and pull-request!

## Run the page locally using Jekyll

To run locally, follow instruction [here](https://jekyllrb.com/) to install Jekyll then run `jekyll serve` to see in `localhost:4000`. Here is a brief install guidelines.

```bash
sudo gem install jekyll
sudo gem install rouge
jekyll serve
```

## Editing the lab website

### Add yourself

You can add yourself to the page in `_people` folder just create file name `<firstname>_<lastname>.md` in the folder. We require few line of header before you start writing your own page. See the following for the header

``` markdown
---
name: Eva Dyer
position: researcher
avatar: eva.jpg
twitter:
joined: 2014
---
```

If you don't have information, just leave it blank. The avatar will bring photo from `images/people` folder and display it on people page.
For lab position, you can choose position from 2 classes including `pi` and `researcher` (so called Honorary members). Position will put you into section that you choose.

We offer a template file `_people/firstname_lastname.md` to help you easily make your page. 

### Edit other pages

You can edit the front page by editing `index.html`,
and other pages by editing markdown files in `_pages`.
These pages are in charge of the PI; thus, change these only when you find some typos.
