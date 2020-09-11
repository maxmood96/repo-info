## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:65c5596ef7aacf0a024c25f7edb9e1b32011215d8365f27d4510f9e8721e2935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:eead9b379e0bb9b7dbcccf95e8daba5fe18e4a5a141eead7045f056e3cbffeae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109993688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5337570e18a4eb3ebcc71f5465d88cf65721dd431b8332a8feae133eaccaa852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:22:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 11 Sep 2020 03:22:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:22:42 GMT
ENV KAPACITOR_VERSION=1.5.6
# Fri, 11 Sep 2020 03:22:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Sep 2020 03:22:46 GMT
EXPOSE 9092
# Fri, 11 Sep 2020 03:22:46 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Sep 2020 03:22:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 11 Sep 2020 03:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:22:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a4ffe01703531900ae63d26540ffde791eeeb9edef562a468cf78eeb25918`  
		Last Modified: Fri, 11 Sep 2020 03:23:02 GMT  
		Size: 13.1 MB (13118906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f150ed336d25bee7ef9195279541ae9412961943bc6e7f28ab26d291a7f47e`  
		Last Modified: Fri, 11 Sep 2020 03:23:00 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971831a9009572a8aabc2fd127df982b4d9f564a2cc30b3b5719d0a97f4c0e4d`  
		Last Modified: Fri, 11 Sep 2020 03:23:15 GMT  
		Size: 36.4 MB (36413458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8bd252b2b84983bc6f60677cb87e756d6c7918424c366c653538c9bfc346c9`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8c717fbb9e3e9488ecabc5418c15a17acfd9a7c44db5efcb2f247c71ba71a`  
		Last Modified: Fri, 11 Sep 2020 03:23:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6f96969e5640da27a9099814df57a373f39a489f0307baeae38bc83215860772
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccc138a73017badc1dafbc7db36956cd2f257674020a91be3416774b52a93ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:52:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:52:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:52:34 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:52:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:52:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:52:43 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:52:44 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:52:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:52:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75cf43b24edcf3677bb001f8f6712c6d3bb022a07985d07975c043341b1e85`  
		Last Modified: Thu, 10 Sep 2020 22:53:01 GMT  
		Size: 13.3 MB (13285643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574d27101ee6986e442ec28fabe44786b74e0483a20f8843d082ccb83e88f30f`  
		Last Modified: Thu, 10 Sep 2020 22:52:59 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3525b18c34520931d2ef62cd55424b6f02beb7f5de39c0f0f723112f349c30`  
		Last Modified: Thu, 10 Sep 2020 22:53:25 GMT  
		Size: 34.1 MB (34140796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e4d39bce2f6964424640cd5367a9e12887c160699bf9d5d2fd628bec85af2`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41931ff6aa8b929f680ff158a6307c2edb2f91e2c312e764966432891a694b5`  
		Last Modified: Thu, 10 Sep 2020 22:53:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:008fac5720dca73b0f694a75f8908a2558b152e709a872546b0fe7b817ff9e00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103707279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfff79a8ccab1b685dadf209845ac003c5a8c8e442e835ecb3dc9521148404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 22:10:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 10 Sep 2020 22:10:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 22:11:00 GMT
ENV KAPACITOR_VERSION=1.5.6
# Thu, 10 Sep 2020 22:11:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 10 Sep 2020 22:11:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 10 Sep 2020 22:11:08 GMT
EXPOSE 9092
# Thu, 10 Sep 2020 22:11:09 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 10 Sep 2020 22:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 10 Sep 2020 22:11:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 22:11:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22516f755571abeef68a3fb7443a74dbdc920a646146d537a19d039fbe830cc9`  
		Last Modified: Thu, 10 Sep 2020 22:11:26 GMT  
		Size: 12.8 MB (12823494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9439323c8548ace51650ae2fb17736a08ec0be37bb0126338e6ff56147ed5f`  
		Last Modified: Thu, 10 Sep 2020 22:11:23 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87328495ff8fed6ae5ad77111ca5ff805bdc871f4e555df953de136a6d00050`  
		Last Modified: Thu, 10 Sep 2020 22:11:48 GMT  
		Size: 33.9 MB (33912757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d44b1e84a03a27d6f6b494b5f7dec4505d8f389eda17a47a7a7d1a5fc30705`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdaaf0d42a7b9c1f5d5b4f8b8c130d900daf095f982e208e1883671a4009bab`  
		Last Modified: Thu, 10 Sep 2020 22:11:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
