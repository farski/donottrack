# donottrack

Simple rack middleware utility to make sure the upcoming standard DNT header is always available. This will normalize things like the X-Do-Not-Track header that may be floating around, allow for server override, and default to 0 (allow tracking, the proposed browser default) if there's no better option.

### Installation

	gem install donottrack
	
### Usage
	# Default behavior
	use Rack::DoNotTrack
	
	# Manual override (always enable do not track)
	use Rack::DoNotTrack, 1
	
Both of these will ensure that, in Rails for instance, request.headers['HTTP_DNT'] will always be available.


## Copyright

Copyright (c) 2011 Chris Kalafarski. See LICENSE.txt for further details.