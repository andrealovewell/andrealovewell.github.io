---
layout: post
title:      "Sort_by in Ruby"
date:       2019-03-26 06:23:11 +0000
permalink:  sort_by_in_ruby
---



While doing my CLI project review I got stuck on sort by in the coding and how to sort something in asceding order. I have coding experience in other languages but not so much in Ruby and some times that can be my downfall. Currently right now I am jumping back and forth between coding in Ruby for Flatiron and also coding in C for my BS degree. So when I was asked to do sort by I had a total C programming response vs a Ruby response. I was like "Oh you are going to be evaluating the character of the first index of that string in that array etc etc etc." and for the block, I said you have to put i, since i is the universal term for refering to an index within an array. Anyways once I got done with the review it took me about 2 seconds to find what  I was looking for.  Coding on the spot has never been my strong suit.

To take cities and then alphabatize them you would do it like this:

@@all = []

def weather_status(userInput)
    puts "Here is the weather data"
    @tracking = Tracking::ZipCode.scrape_weatherStreet(userInput)
		puts " Temperature: #{@tracking[0]}, City: #{@tracking[1]}, Visibility: #{@tracking[2]}, Wind: #{@tracking[3]}"
		@@all << #{@tracking[2]}
		
  end

def self.cities_sorted
    @@all.sort_by { |city| city .downcase}
		@@all
	end
	
	or
	
	def self.cities_sorted
	    @@all.sort
	end

