---
title: Change Text alignment on UIPickerView
layout: post
date: 2012-10-23 02:14:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS Programming
---
Use '<i>viewForRow</i>' instead of '<i>titleForRow</i>', like this:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> // Used this instead of titleForRow to allow center aligment of text  <br /> - (UIView *)pickerView:(UIPickerView *)pickerView viewForRow:(NSInteger)row forComponent:(NSInteger)component reusingView:(UIView *)view  <br /> {  <br />   UILabel *label = [[UILabel alloc] init];  <br />   //For center alignment of text  <br />   [label setTextAlignment:UITextAlignmentCenter];  <br />   label.opaque=NO;  <br />   label.backgroundColor=[UIColor clearColor];  <br />   label.textColor = [UIColor blackColor];  <br />   UIFont *font = [UIFont boldSystemFontOfSize:20];  <br />   label.font = font;  <br />   [label setText:[NSString stringWithFormat:@"%d", row]];  <br />   return label;  <br /> }  <br /></code></pre><br /><a href="http://stackoverflow.com/a/4366010">Source</a>