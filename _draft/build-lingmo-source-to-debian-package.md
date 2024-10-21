

##
## ## Link
##
## * https://github.com/LingmoOS/lingmo-build
## * https://github.com/LingmoOS/lingmo-build/blob/main/Modules/BuildUtils.psm1
## 
##


##
## ## Install-GlobalDepends
##

sudo apt-get --yes install git devscripts equivs




##
## ## Install-RepoDepends
##

sudo mk-build-deps -i -t "apt-get -y" -r


##
## ## Start-CompileDeb
##


dpkg-buildpackage -b -uc -us -tc -j$(nproc)
