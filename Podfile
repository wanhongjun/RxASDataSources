# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'Example' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  pod 'Texture'
  pod 'RxSwift'
  pod 'RxCocoa'
  pod 'Differentiator'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.name == 'PINCache' || target.name == 'PINOperation' || target.name == 'PINRemoteImage' then
      target.build_configurations.each do |configuration|
        configuration.build_settings['OTHER_CFLAGS'] = '-Xclang -fcompatibility-qualified-id-block-type-checking'
      end
    end
  end
    
end
