# Uncomment this line to define a global platform for your project
platform :ios, '11.0'

target 'CustomVisionModelforCoreMLwithWatsonMWDGW' do
    pod 'BMSCore', '~> 2.0'

    # Comment this line if you're not using Swift and don't want to use dynamic frameworks
    use_frameworks!

    pod "SwiftSpinner", '~> 1.5.0'

    post_install do |installer|
        installer.pods_project.targets.each do |target|
            if ['SwiftCloudant', 'SwiftSpinner'].include? target.name
                target.build_configurations.each do |config|
                    config.build_settings['SWIFT_VERSION'] = '3.2'
                end
            end
        end
    end
end
