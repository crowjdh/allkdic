platform :osx, '10.15'

target 'Allkdic' do
  use_frameworks!

  pod 'SnapKit', '~> 5.0'

  target 'AllkdicTests' do
    inherit! :search_paths
  end

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '5.0'
      config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.15'
    end
  end
end
