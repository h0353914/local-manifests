Installing Repos

        repo init -u https://github.com/LineageOS/android.git -b lineage-22.1 --git-lfs

        git clone https://github.com/h0353914/local-manifests.git -b lineage-22.1 .repo/local_manifests/
        
sync repo

        repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Signing builds:

        bash <(curl -Ls https://raw.githubusercontent.com/ATI-labs/local-manifests/sign/sign.sh)

running build
        
        . build/envsetup.sh
        brunch {device} user
