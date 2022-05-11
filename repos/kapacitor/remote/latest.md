## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:51e6e692564e09f1cacafa1526b486ddb228e040fd100a899e5b568c7096995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:12683525b8aadd049bbb22c3d51d91e1c009a0d114d35f98469e25bbe4b6ce9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135231814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4f2e21e2a902417b6ca2f4e7bf8e0c25b644e311a3de0bd0d69e0c222d7ef8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 11 May 2022 01:22:05 GMT
ADD file:00f57642edc8479d50e6470a3509ad679eb9353761912deade33251fb3d9daa8 in / 
# Wed, 11 May 2022 01:22:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 20:19:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 11 May 2022 20:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 20:19:20 GMT
ENV KAPACITOR_VERSION=1.6.4
# Wed, 11 May 2022 20:19:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 11 May 2022 20:19:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 11 May 2022 20:19:27 GMT
EXPOSE 9092
# Wed, 11 May 2022 20:19:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 May 2022 20:19:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 11 May 2022 20:19:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 20:19:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:06e39e28714dba08fe310ca1aafb43905427729ecf8e9586f811a7e5062fd09b`  
		Last Modified: Wed, 11 May 2022 01:28:34 GMT  
		Size: 45.4 MB (45428005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2141afc44a4cc9b8f9bd9ae1ad4ec8921fdf75b6be9b192b60f1b7f8469919`  
		Last Modified: Wed, 11 May 2022 02:00:35 GMT  
		Size: 11.3 MB (11302273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38533702160421fc5a777d84e162c51816a24426e58139f426e8156fef69d7a7`  
		Last Modified: Wed, 11 May 2022 02:00:34 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba195b4bc21ef3724f088897d1aac8e7068de1417a81ee5d80a4b8e0092a038`  
		Last Modified: Wed, 11 May 2022 20:19:47 GMT  
		Size: 13.4 MB (13413735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9ee354c8a8e72692bd91bae5e779d1ca41bd63a0437089cb5e7cb46629d412`  
		Last Modified: Wed, 11 May 2022 20:19:46 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491e40cfb28334046f70a3c70214a052de63e68cb16450865444c462fdd3f51a`  
		Last Modified: Wed, 11 May 2022 20:20:09 GMT  
		Size: 60.7 MB (60741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2763a3617f4aa0a2e4415718effb031aedcf1a18bc26845c46c9d5e3a1a0cb0`  
		Last Modified: Wed, 11 May 2022 20:20:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249e566eed48ae124d6205ee9f5d5a6342a3e4e89e1273d9abc38cbc3fc1fad4`  
		Last Modified: Wed, 11 May 2022 20:20:01 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a0ea377d14794289194320acc8cd74433d7bba0275cd30355faa9104b95f3a62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127199217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec513cad13280cdf4cf04a414c22fdd873882f4b348ae97d0ba9b86f7363b556`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 11 May 2022 00:49:08 GMT
ADD file:8949016fba61b18207f5a2309fc974562080c5cc80d1eb82adb35c4fa03f6f05 in / 
# Wed, 11 May 2022 00:49:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:29:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:30:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 19:53:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 11 May 2022 19:53:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 19:53:25 GMT
ENV KAPACITOR_VERSION=1.6.4
# Wed, 11 May 2022 19:53:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 11 May 2022 19:53:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 11 May 2022 19:53:31 GMT
EXPOSE 9092
# Wed, 11 May 2022 19:53:32 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 May 2022 19:53:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 11 May 2022 19:53:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 19:53:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:139065d8f4553df403babda56f830c32aa1f3e57f18d2145a3179468921a4bb8`  
		Last Modified: Wed, 11 May 2022 00:57:26 GMT  
		Size: 43.2 MB (43212478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0acfd1725613d968a54b7fbfe1f70f24b8a0dad792ad3cb28349035f7736fe`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 10.2 MB (10217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c314192ef0350d2ac1d1e49b4fddbc49dbcdc609e56e0e2567ee2dd37f0bc`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 3.9 MB (3874525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496f27b7f192b22433c9935e31905643e2224453cec24dd8a895fbc0ed124a61`  
		Last Modified: Wed, 11 May 2022 19:53:54 GMT  
		Size: 12.9 MB (12895614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865c958dbaf4cdc7c502e2fa2e224ecd728970e3f5a6624c291b06f0f0fe724`  
		Last Modified: Wed, 11 May 2022 19:53:53 GMT  
		Size: 2.8 KB (2822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9600783cb63804ab90b3c37bfc621d2f9ea15f4bc9aa6cf53f71f7ced8942550`  
		Last Modified: Wed, 11 May 2022 19:54:16 GMT  
		Size: 57.0 MB (56995547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb592b11071788c11c6233720ccfb56da4a2482aefa1388006bbd475bdfefd3`  
		Last Modified: Wed, 11 May 2022 19:54:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdfaac5862ab10711f77f97e571ce72394d53fb4584c1f3ba2a8d767228ea2d`  
		Last Modified: Wed, 11 May 2022 19:54:09 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
