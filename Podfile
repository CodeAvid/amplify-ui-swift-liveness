platform :ios, '14.0'

target 'FaceLiveness' do
  use_frameworks!
  
  # AWS Amplify dependencies
  pod 'Amplify', '2.42.1'
  pod 'AWSPluginsCore', '2.42.1'
  pod 'AWSCognitoAuthPlugin', '2.42.1'
  pod 'AWSPredictionsPlugin', '2.42.1'
  
  target 'FaceLivenessTests' do
    inherit! :search_paths
  end
end

# Post-install handling for resources
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      # Ensure minimum iOS version
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '14.0'
    end
  end
end
