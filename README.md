## react-native-view-more-text

A super lightweight plugin to expand/collapse text in React-Native. Truncated text is ended with dotdotdot.

Working on IOS/Android

### Installation

```
npm install --save react-native-view-more-text 

```

### Usage

- **numberOfLines**(required): Number of lines to be displayed.
- **truncatedHeight**(required): If the text exceeds this height, truncation will be triggered.
- **renderViewMore**: Render view-more component 
- **renderViewLess**: Render view-less component 

```javascript
	import ViewMoreText from 'react-native-view-more-text';
	
	let Example = React.createClass({
		renderViewMore(onPress){
			return(
      	<Text onPress={onPress}>View more</Text>
    	)
		},
		renderViewLess(onPress){
			return(
      	<Text onPress={onPress}>View less</Text>
    	)
		},
		render(){
			return(
				<ViewMoreText
			    numberOfLines={3}
			    truncatedHeight={50}
			    renderViewMore={this.renderViewMore}
			    renderViewLess={this.renderViewLess}>
			    <Text>
			      Lorem ipsum dolor sit amet, in quo dolorum ponderum, nam veri molestie constituto eu. Eum enim tantas sadipscing ne, ut omnes malorum nostrum cum. Errem populo qui ne, ea ipsum antiopam definitionem eos.
			    </Text>
			  </ViewMoreText>
			)
		}
	})

```