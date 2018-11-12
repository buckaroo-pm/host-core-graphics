genrule(
  name = 'core-graphics-framework', 
  out = 'CoreGraphics.framework', 
  cmd = 'cp -r /System/Library/Frameworks/CoreGraphics.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'core-graphics', 
  framework = ':core-graphics-framework', 
  preferred_linkage = 'static', 
  visibility = [
    'PUBLIC', 
  ], 
)
