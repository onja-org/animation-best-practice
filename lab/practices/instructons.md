# CSS Animation Practice Session
**Duration: 45 Minutes | Level: Beginner**

---

## 📅 Session Timeline

| Time | Exercise | Focus |
|------|----------|-------|
| **0-10 min** | Exercise 1 | Basic Hover Effects |
| **10-20 min** | Exercise 2 | Simple @keyframes Animation |
| **20-35 min** | Exercise 3 | Interactive Button with Multiple Effects |
| **35-45 min** | Exercise 4 | Card Animation Challenge |

---

## 🎯 Learning Objectives

By the end of this session, students will be able to:
- Create smooth hover animations using CSS transitions
- Build entrance animations with @keyframes
- Combine multiple animation techniques
- Apply performance-friendly animation properties
- Implement basic accessibility considerations

---

## Exercise 1: Basic Hover Effects
**⏰ Time: 10 minutes**

### 🎯 Objective
Create a button that smoothly changes color and lifts up when hovered over.

### 📝 What Students Need to Create
A button with the following specifications:
- Default state: Blue background (#3498db), white text
- Hover state: Darker blue (#2980b9), lifts up 3px, shows shadow
- Smooth transition between states (0.3 seconds)

### 🛠️ HTML Structure Needed
```html
<button class="hover-button">Hover Me!</button>
```

### 📋 Step-by-Step Tasks
1. **Set up the button base styles:**
   - Padding: 15px 30px
   - Background: #3498db
   - White text, no border
   - Border radius: 5px
   - Cursor pointer, font size 16px

2. **Add smooth transitions:**
   - Use `transition: all 0.3s ease;`

3. **Create hover effects:**
   - Change background to #2980b9
   - Add `transform: translateY(-3px)`
   - Add box-shadow: `0 4px 8px rgba(0,0,0,0.2)`

4. Check video bellow and compare to your result

<video width="640" height="360" controls>
  <source src="./video/hover-button.mp4" type="video/mp4" />
</video>


### ✅ Success Criteria
- Button color changes smoothly on hover
- Button lifts up with shadow effect
- Animation reverses when hover ends
- Total animation feels smooth and natural


### 💡 Common Mistakes to Avoid
- Don't forget the transition property on the base element
- Avoid animating non-performant properties like `top` or `margin-top`

---

## Exercise 2: Simple @keyframes Animation
**⏰ Time: 10 minutes**

### 🎯 Objective
Create a colored box that bounces in when the page loads using @keyframes.

### 📝 What Students Need to Create
A box with these specifications:
- 200px × 200px red square (#e74c3c)
- Rounded corners (10px)
- Contains centered text "I'm Animated!"
- Animates in with bounce effect on page load

### 🛠️ HTML Structure Needed
```html
<div class="animated-box">
    <h3>I'm Animated!</h3>
</div>
```

### 📋 Step-by-Step Tasks
1. **Create the box base styles:**
   - Width/height: 200px
   - Background: #e74c3c
   - Border-radius: 10px
   - Center the text with flexbox
   - White text color

2. **Create @keyframes bounceIn:**
   - **0%:** `opacity: 0; transform: translateY(-50px);`
   - **60%:** `opacity: 1; transform: translateY(10px);`
   - **100%:** `opacity: 1; transform: translateY(0);`

3. **Apply the animation:**
   - Use `animation: bounceIn 1s ease-out;`

4. **Test the animation:**
   - Refresh the page to see the effect
   - Box should start invisible and above, then drop with a bounce

5. **Compare your result to the video bellow**

<video width="640" height="360" controls>
  <source src="./video/red-box.mp4" type="video/mp4" />
</video>

### ✅ Success Criteria
- Box starts invisible and positioned above final location
- Fades in while dropping down
- Has small bounce before settling
- Animation runs once on page load

### 💡 Teaching Points
- Explain why we use `transform: translateY()` instead of changing `top`
- Show how keyframe percentages work
- Discuss `ease-out` timing (fast start, slow end)

---

## Exercise 3: Interactive Button with Multiple Effects
**⏰ Time: 15 minutes**

### 🎯 Objective
Create an advanced button that combines entrance animation with hover interactions.

### 📝 What Students Need to Create
A button featuring:
- Gradient background (orange to red)
- Slides in from left while scaling up on page load
- Multiple hover effects: scale, glow, brightness
- Smooth transitions for all interactions

### 🛠️ HTML Structure Needed
```html
<button class="super-button">
    <span>Click Me!</span>
</button>
```

### 📋 Step-by-Step Tasks

#### Part A: Base Button Styling (3 minutes)
1. **Style the button:**
   - Padding: 20px 40px
   - Background: `linear-gradient(45deg, #ff6b6b, #ee5a24)`
   - White text, no border
   - Border-radius: 25px
   - Font: 18px, bold
   - Position: relative, overflow: hidden

#### Part B: Entrance Animation (7 minutes)
2. **Create slideInScale keyframes:**
   - **0%:** `transform: translateX(-100px) scale(0.5); opacity: 0;`
   - **100%:** `transform: translateX(0) scale(1); opacity: 1;`

3. **Apply entrance animation:**
   - Use `animation: slideInScale 0.8s ease-out;`

#### Part C: Hover Effects (5 minutes)
4. **Add smooth transitions to super button:**
   - `transition: all 0.3s ease;`

5. **Create hover effects:**
   - Scale: `transform: scale(1.05);`
   - Glow: `box-shadow: 0 8px 20px rgba(255, 107, 107, 0.4);`
   - Brightness: `filter: brightness(1.1);`
6. **Compare your result to the video bolow**

<video width="640" height="360" controls>
  <source src="./video/orange.mp4" type="video/mp4" />
</video>



### ✅ Success Criteria
- Button slides in from left while growing on page load
- Smooth hover effects that combine scale, shadow, and brightness
- All animations feel coordinated and professional
- No performance issues or janky animations

### 🌟 Bonus Challenge
Add a subtle pulse animation that runs continuously:
```css
@keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.02); }
}
```
Apply with: `animation: slideInScale 0.8s ease-out, pulse 2s ease-in-out infinite 1s;`

# Exercise 4: Card Animation Challenge
**⏰ Time: 10 minutes**

---

## 🎯 Objective
Create a complete animated card component that demonstrates all learned concepts plus accessibility.

## 📝 What Students Need to Create
An animated card with:
- Card entrance animation from bottom
- Icon rotation on hover
- Card lift effect with glow
- Interactive button
- Accessibility support

## 🛠️ HTML Structure Needed
```html
<div class="challenge-card">
    <div class="card-icon">🚀</div>
    <h3>Amazing Card</h3>
    <p>This card has multiple animations working together!</p>
    <button class="card-button">Learn More</button>
</div>
```

## 📋 Step-by-Step Tasks

### Part A: Card Base & Entrance (4 minutes)

#### 1. **Style the card:**
   - Background: white
   - Padding: 2rem
   - Border-radius: 15px
   - Box-shadow: `0 4px 15px rgba(0,0,0,0.1)`
   - Max-width: 300px
   - Center with `margin: 0 auto`
   - Text-align: center
   - Add smooth transitions with `transition: all 0.3s ease`

#### 2. **Create card entrance animation:**
   - Create **fadeInUp keyframes:** 
     - **0%:** `opacity: 0; transform: translateY(30px) scale(0.9);`
     - **100%:** `opacity: 1; transform: translateY(0) scale(1);`
   - Apply to card: `animation: fadeInUp 0.8s ease-out;`

### Part B: Interactive Effects (4 minutes)

#### 3. **Card hover effects:**
   - On hover: `transform: translateY(-8px);`
   - On hover: `box-shadow: 0 15px 30px rgba(0,0,0,0.2);`

#### 4. **Icon styling and animation:**
   - Font-size: 3rem
   - Margin-bottom: 1rem
   - Add smooth transitions with `transition: all 0.3s ease`
   - **IMPORTANT:** Icon rotates only when **card** is hovered (use `.challenge-card:hover .card-icon`)
   - On card hover: `transform: rotate(10deg) scale(1.1);`

#### 5. **Button styling:**
   - Padding: 12px 24px
   - Background: #007bff
   - White text, no border
   - Border-radius: 8px
   - Font-size: 14px, font-weight: bold
   - Cursor: pointer
   - Add smooth transitions with `transition: all 0.3s ease`
   - On hover: background changes to #0056b3
   - On hover: `transform: scale(1.05)`
   - On hover: `box-shadow: 0 4px 8px rgba(0,0,0,0.2)`

### Part C: Accessibility (2 minutes)

#### 6. **Add reduced motion support:**
   - Create media query for `(prefers-reduced-motion: reduce)`
   - Target all elements with `*`
   - Set `animation-duration: 0.01ms !important`
   - Set `animation-iteration-count: 1 !important`
   - Set `transition-duration: 0.01ms !important`

## 🌟 Final Challenge: Staggered Animations

Create a cascade effect where elements appear one after another:

#### **Animation Sequence:**
- **Card:** no delay → `animation: fadeInUp 0.8s ease-out;`
- **Icon:** 0.2s delay → `animation: fadeInUp 0.8s ease-out 0.2s both;`
- **Title (h3):** 0.4s delay → `animation: fadeInUp 0.8s ease-out 0.4s both;`
- **Text (p):** 0.6s delay → `animation: fadeInUp 0.8s ease-out 0.6s both;`
- **Button:** 0.8s delay → `animation: fadeInUp 0.8s ease-out 0.8s both;`

#### **Style the text elements:**
- **h3:** Color: #2c3e50, margin-bottom: 1rem
- **p:** Color: #7f8c8d, line-height: 1.6, margin-bottom: 1.5rem

**Critical:** Use `both` keyword for delayed animations to keep elements invisible until their animation starts.

<video width="640" height="360" controls>
  <source src="./video/card-robot.mp4" type="video/mp4" />
</video>

## ✅ Success Criteria
- ✅ Card animates in smoothly from bottom with scale effect
- ✅ Card lifts up and shows enhanced shadow on hover
- ✅ Icon rotates and scales **only** when card is hovered (not always)
- ✅ Button has proper color (#007bff) and hover effects (#0056b3)
- ✅ Elements appear with staggered delays (0.2s, 0.4s, 0.6s, 0.8s intervals)
- ✅ Text elements have proper colors and spacing
- ✅ Accessibility media query is included for reduced motion
- ✅ All animations feel coordinated and professional

## 💡 Key Teaching Points

### **Performance Best Practices:**
- Always use `transform` for movement (translateY, scale, rotate)
- Use `opacity` for fade effects
- Avoid animating `top`, `left`, `margin`, `width`, or `height`

### **Animation Timing:**
- Entrance animations: 0.8s (natural feeling)
- Hover transitions: 0.3s (responsive feeling)
- Staggered delays: 0.2s intervals (creates rhythm)

### **Selector Importance:**
- `.card-icon` styles the icon always
- `.challenge-card:hover .card-icon` styles icon only when card is hovered

### **Animation Fill Modes:**
- `both` applies keyframe styles before and after animation
- Essential for staggered animations to prevent flash of unstyled content

### **Accessibility Considerations:**
- Always include `prefers-reduced-motion` media query
- Respect users who prefer less motion
- Test with reduced motion settings enabled

## 🚨 Common Mistakes to Avoid

❌ **Icon Animation Mistakes:**
- Don't make icon always rotated
- Don't use wrong selector (`icon:hover` instead of `card:hover icon`)

❌ **Color Mistakes:**
- Don't use wrong button color (#3498db instead of #007bff)
- Don't use generic color names (darkblue instead of #0056b3)

❌ **Animation Mistakes:**
- Don't forget `animation-fill-mode: both` for delayed animations
- Don't use fixed positioning or margins for movement
- Don't forget the accessibility media query
- Don't skip styling the h3 and p elements

❌ **Layout Mistakes:**
- Don't use fixed widths that break on mobile
- Don't forget to center the card properly

## 🎯 Testing Your Work

1. **Refresh the page** - All elements should appear in sequence
2. **Hover over the card** - Should lift with shadow, icon should rotate
3. **Hover over the button** - Should change color and scale slightly
4. **Check accessibility** - Enable "Reduce motion" in browser settings

---

**🎉 End Result:** A professional animated card component that demonstrates smooth entrance animations, coordinated hover effects, and accessibility best practices!

---

## 🎓 Session Wrap-up

### What Students Have Learned
✅ **CSS Transitions** - Smooth property changes on state changes  
✅ **@keyframes Animations** - Complex, multi-stage animations  
✅ **Animation Timing** - Choosing appropriate durations and easing  
✅ **Performance Best Practices** - Using transform and opacity  
✅ **Accessibility Considerations** - Respecting user preferences  
✅ **Real-world Application** - Combining techniques in practical components  

### Key Takeaways
- **Performance:** Always use `transform` and `opacity` when possible
- **Timing:** Keep UI animations under 1 second
- **Purpose:** Every animation should enhance user experience
- **Accessibility:** Always include `prefers-reduced-motion`
- **Testing:** Refresh page to test entrance animations

### Next Steps for Students
1. **Practice:** Apply these techniques to personal projects
2. **Explore:** Research CSS animation libraries and advanced techniques
3. **Study:** Look at well-designed websites for animation inspiration
4. **Experiment:** Try combining animations with JavaScript for dynamic effects

---

## 📚 Quick Reference

### Essential Properties
- `transition: property duration timing-function;`
- `animation: name duration timing-function delay iteration-count;`
- `transform: translateX() translateY() scale() rotate();`
- `animation-delay: time;`
- `animation-fill-mode: both;`

### Performance-Friendly Properties
✅ **Good:** `transform`, `opacity`, `box-shadow`, `filter`  
❌ **Avoid:** `width`, `height`, `top`, `left`, `margin`, `padding`

### Common Timing Functions
- `ease` - Default, slow start and end
- `ease-in` - Slow start
- `ease-out` - Slow end (best for entrances)
- `ease-in-out` - Slow start and end
- `linear` - Constant speed

**End of Practice Session**