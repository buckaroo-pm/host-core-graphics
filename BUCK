xcode_developer_dir = read_config('apple', 'xcode_developer_dir', '/Applications/Xcode.app/Contents/Developer')

genrule(
  name = 'core-graphics-framework', 
  out = 'CoreGraphics.framework', 
  cmd = 'cp -r ' + xcode_developer_dir + '/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/CoreGraphics.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'core-graphics', 
  framework = ':core-graphics-framework', 
  preferred_linkage = 'static', 
  deps = [
    'buckaroo.github.buckaroo-pm.host-core-foundation//:core-foundation', 
  ], 
  visibility = [
    'PUBLIC', 
  ], 
)
