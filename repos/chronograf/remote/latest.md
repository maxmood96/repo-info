## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1afe04050c8d702be216a813a21ef7e340e16b7fc4fb5f3a778a38db3581f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:380dde297f323ba57a0b07ca849a6c7582e05a7cd52577d44dce054bb502d2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84101080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a8a073dfc63164af1a2f1bd67da6e4fbda63b5b6c1e8b8ab05060fac70496d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:46:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:29 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 10:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:38 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1956287ac9cfdc19991d482f7cfe094a5236d159dca178b0e4e2888989901d13`  
		Last Modified: Tue, 21 Nov 2023 10:47:39 GMT  
		Size: 7.9 MB (7873073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb62f985c03da59f7ba67ba98ea4eff8aac143fc92e81898567003bca5c00af`  
		Last Modified: Tue, 21 Nov 2023 10:47:43 GMT  
		Size: 47.1 MB (47053706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b385f9ed0e852b69a364d9c189f846eb9f1df339ad58cb86610d69e86d8cb4`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb06199f978c7bf17a871d0668ac1245f63349368d3a416f8788268c921a171`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5e09745fe375af5895b0b1c99d8110d4704ec58d7c7df8619dc1622f8dcc`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3024f41d59a015cc2c86ad2aa2e0f1abb4b882b9345c6a43f7b600bf2d8af65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2332571a6259070e1637d40b140c79fa917f32e446565a38a7a90649f0b12b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:02:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:02:00 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:02:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:02:10 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:02:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:02:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:02:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:02:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a72f2ea3c3dd4c6c84869aff33141879c89aed7d1ebdee23dd5cc143fbe8c2`  
		Last Modified: Tue, 21 Nov 2023 07:03:02 GMT  
		Size: 6.5 MB (6497812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26311c9696c337908f2631c213e79d0c72849a72085fde9380f35a1c67ed28fa`  
		Last Modified: Tue, 21 Nov 2023 07:03:08 GMT  
		Size: 44.6 MB (44649586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8f1e393f681f858ed71dbc056c8a255df814677dc93f57014c85a6411f5bc`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c8c90cbbd08d52d14449a9108f380a4fd480b83a4a28fdef9ccae09f49738f`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527e2aad92573d1f8276fe9286d5379b57115a489a28173509391bf2c65c2a3`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:907da70564d00845356dabad9cb329f113e7642486d3ec24208ea93466beb07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9355053d09268aef0f21bada565fd0029a482328b07884f0e71fcc8b9834721d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:56:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:56:05 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:56:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:56:13 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:56:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:56:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f93356fcd55f6426d456c26d4a5e38da0bb544a18f1666780fa447b8eed55d`  
		Last Modified: Tue, 21 Nov 2023 07:57:00 GMT  
		Size: 7.6 MB (7649760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3d345558481a7c6da4301adcd44374730662770cf8edb7b7c82f9c44ad26`  
		Last Modified: Tue, 21 Nov 2023 07:57:04 GMT  
		Size: 44.8 MB (44773832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1417ae54eecd2b37aef5ab9b854f4a8641033587d30e3ce30f765091c47afd4`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dd685ae00f8ca4c49f165c1dc572de1b4e2510dcdbb20a96f9b963a831e69`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace178832cf7524abb72847cc73615fb748c94a3583f08add64d5938d2d0512`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
