<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.7`](#kapacitor157)
-	[`kapacitor:1.5.7-alpine`](#kapacitor157-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:c165de0365e5e3b5706661db38790c844fb681f16df4cc673f3511c04c18c03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:c4ad6ad9f4b225b76aa7e90447330e6ee0e23abe7d4063314fb6b095ca9013e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96388582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b6efffcaeff9e78f1681b3582f8328b7bb918bc7cb886a524d5b4fee40ce70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 17:16:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 12 Dec 2020 17:16:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 17:16:12 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 12 Dec 2020 17:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 17:16:15 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 12 Dec 2020 17:16:16 GMT
EXPOSE 9092
# Sat, 12 Dec 2020 17:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 12 Dec 2020 17:16:16 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 12 Dec 2020 17:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 17:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76813506a5b5f42603d3e7dd21ffcdbc93ecd54b131c1e5ebe9c38e370b3e296`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 13.2 MB (13220305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a4d029641aa49b3d0d084b453a50e8a3e67bff3662df5fc87ffaf20a9066e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaca1b5412a5a939646a13f832c2dcd90fc96de74c13d453cde6ff15fe5dcbd7`  
		Last Modified: Sat, 12 Dec 2020 17:16:54 GMT  
		Size: 22.7 MB (22694277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf559dcb4316cdf3734c89e1dfed2d57f129b39ac829f3b1c6c8ee4ae2424e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d452a2af7a5105e429908d47d1e95191be6d849e74bdb56d9ca633ef7d04c6f`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:76afd24ef6b608c55a8bf96fb70a52e7bf91fbe1923f8a069eaebabdf3525957
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90192038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afd37a406dafcd20c71354dea6c9f9fcb0bb57bfb2fe8f3832ea60e19810c71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:05:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 18:05:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:05:33 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 18:05:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:05:40 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 18:05:41 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 18:05:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 18:05:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 18:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:05:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b64fd1085dc49f926810d3b22f9ad70b1ad5fe33ba9e372ca1655daf1247bc6`  
		Last Modified: Thu, 17 Dec 2020 18:06:22 GMT  
		Size: 13.4 MB (13397499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd7af3576c6b4584d4ddd1b4600001e002c1df436221db37dcd3ce7b116e71`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3970745cc641979d9f205c7c5dc26c7f04f73a6a5692617c4699fe8dca1b927`  
		Last Modified: Thu, 17 Dec 2020 18:06:28 GMT  
		Size: 21.3 MB (21308098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ed043c163b685f0765ec01d0e2b917c2d7145c3862ab1f64773c82a1cf631`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1121e3732e0f8f7324dddf03f1eedcbd5a75bf38f3be01d04520ee34c91fdd9`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:55eab130974cb9f74057279d8ff5dad2d38a12b04f9156da5013cb3d3239c298
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91211764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837281db728843960a4f78540fd3577fa470a8762f27d183bd06665692196d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:29:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 15:29:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:29:18 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 15:29:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:29:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 15:29:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 15:29:38 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 15:29:39 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 15:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:29:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e581a3c8d8ee45a1b2b7bda76c01a7ea09dcf9be92fc9d7a3adfb7ffc785e1`  
		Last Modified: Thu, 17 Dec 2020 15:30:26 GMT  
		Size: 12.9 MB (12926186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3bb5990a1ae62a743fbe010b3203a06825b9dcd10b8de203bf1a7e34d2c8e4`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d678907ff8c4134417cc538fea539a19e8e418dcd6e0be3406b29bbd2d060`  
		Last Modified: Thu, 17 Dec 2020 15:30:30 GMT  
		Size: 21.3 MB (21307934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc0324644dc86faf79f9c1eeb02cbd821b0b7614db929ec5b9a0d94d0a7e500`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c408569f0473f1f66766ea8cd2cfee98080532fa27de5e4f20c86d25fbba813`  
		Last Modified: Thu, 17 Dec 2020 15:30:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:c165de0365e5e3b5706661db38790c844fb681f16df4cc673f3511c04c18c03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:c4ad6ad9f4b225b76aa7e90447330e6ee0e23abe7d4063314fb6b095ca9013e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96388582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b6efffcaeff9e78f1681b3582f8328b7bb918bc7cb886a524d5b4fee40ce70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 17:16:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 12 Dec 2020 17:16:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 17:16:12 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 12 Dec 2020 17:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 17:16:15 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 12 Dec 2020 17:16:16 GMT
EXPOSE 9092
# Sat, 12 Dec 2020 17:16:16 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 12 Dec 2020 17:16:16 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 12 Dec 2020 17:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 17:16:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76813506a5b5f42603d3e7dd21ffcdbc93ecd54b131c1e5ebe9c38e370b3e296`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 13.2 MB (13220305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a4d029641aa49b3d0d084b453a50e8a3e67bff3662df5fc87ffaf20a9066e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaca1b5412a5a939646a13f832c2dcd90fc96de74c13d453cde6ff15fe5dcbd7`  
		Last Modified: Sat, 12 Dec 2020 17:16:54 GMT  
		Size: 22.7 MB (22694277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf559dcb4316cdf3734c89e1dfed2d57f129b39ac829f3b1c6c8ee4ae2424e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d452a2af7a5105e429908d47d1e95191be6d849e74bdb56d9ca633ef7d04c6f`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:76afd24ef6b608c55a8bf96fb70a52e7bf91fbe1923f8a069eaebabdf3525957
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90192038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afd37a406dafcd20c71354dea6c9f9fcb0bb57bfb2fe8f3832ea60e19810c71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:05:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 18:05:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:05:33 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 18:05:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:05:40 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 18:05:41 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 18:05:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 18:05:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 18:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:05:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b64fd1085dc49f926810d3b22f9ad70b1ad5fe33ba9e372ca1655daf1247bc6`  
		Last Modified: Thu, 17 Dec 2020 18:06:22 GMT  
		Size: 13.4 MB (13397499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd7af3576c6b4584d4ddd1b4600001e002c1df436221db37dcd3ce7b116e71`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3970745cc641979d9f205c7c5dc26c7f04f73a6a5692617c4699fe8dca1b927`  
		Last Modified: Thu, 17 Dec 2020 18:06:28 GMT  
		Size: 21.3 MB (21308098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ed043c163b685f0765ec01d0e2b917c2d7145c3862ab1f64773c82a1cf631`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1121e3732e0f8f7324dddf03f1eedcbd5a75bf38f3be01d04520ee34c91fdd9`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:55eab130974cb9f74057279d8ff5dad2d38a12b04f9156da5013cb3d3239c298
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91211764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837281db728843960a4f78540fd3577fa470a8762f27d183bd06665692196d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:29:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 15:29:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:29:18 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 15:29:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:29:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 15:29:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 15:29:38 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 15:29:39 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 15:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:29:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e581a3c8d8ee45a1b2b7bda76c01a7ea09dcf9be92fc9d7a3adfb7ffc785e1`  
		Last Modified: Thu, 17 Dec 2020 15:30:26 GMT  
		Size: 12.9 MB (12926186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3bb5990a1ae62a743fbe010b3203a06825b9dcd10b8de203bf1a7e34d2c8e4`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d678907ff8c4134417cc538fea539a19e8e418dcd6e0be3406b29bbd2d060`  
		Last Modified: Thu, 17 Dec 2020 15:30:30 GMT  
		Size: 21.3 MB (21307934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc0324644dc86faf79f9c1eeb02cbd821b0b7614db929ec5b9a0d94d0a7e500`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c408569f0473f1f66766ea8cd2cfee98080532fa27de5e4f20c86d25fbba813`  
		Last Modified: Thu, 17 Dec 2020 15:30:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:797102b5cdb633ea9bcd98f02e6df6b81b4ae92971315d982f497676251bb1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a3cd5f7ac34d6ed8bb02192555ef40a3078e4194187e91829fb8690ed985592e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a6cbb3d71432ffe9773020bff6a82308d8bbcdd4796b2befb8b2539249498`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 13:23:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2700961e2aa9d8b1a747e151bac0e7e85eaf621a73e665aa091034cdbb9fa`  
		Last Modified: Thu, 17 Dec 2020 13:24:11 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0945c6384dc59f39c26a68228e5e75d062e8b903846f0dac9ec9822fddba6`  
		Last Modified: Thu, 17 Dec 2020 13:24:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5717d74957dbfe0e93c0cfe6e49d336e9533eea3f7ae7141f42aa72c708d3c63`  
		Last Modified: Thu, 17 Dec 2020 13:24:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:797102b5cdb633ea9bcd98f02e6df6b81b4ae92971315d982f497676251bb1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a3cd5f7ac34d6ed8bb02192555ef40a3078e4194187e91829fb8690ed985592e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a6cbb3d71432ffe9773020bff6a82308d8bbcdd4796b2befb8b2539249498`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 13:23:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2700961e2aa9d8b1a747e151bac0e7e85eaf621a73e665aa091034cdbb9fa`  
		Last Modified: Thu, 17 Dec 2020 13:24:11 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0945c6384dc59f39c26a68228e5e75d062e8b903846f0dac9ec9822fddba6`  
		Last Modified: Thu, 17 Dec 2020 13:24:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5717d74957dbfe0e93c0cfe6e49d336e9533eea3f7ae7141f42aa72c708d3c63`  
		Last Modified: Thu, 17 Dec 2020 13:24:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:0cecb2079c945775ab85c1151089edfcd23799ddae9b4faec568fd62b77f7a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:d3588c0ac35b1ce33e5a1c095092849a0c341be6639f973a0cc97e7d321a9629
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110148872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfb33ff0297a7fbefb06535dcb036b22fadfe69eb48f0aee29352dbc3b8a0e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 17:16:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 12 Dec 2020 17:16:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 17:16:26 GMT
ENV KAPACITOR_VERSION=1.5.7
# Sat, 12 Dec 2020 17:16:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 12 Dec 2020 17:16:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 12 Dec 2020 17:16:30 GMT
EXPOSE 9092
# Sat, 12 Dec 2020 17:16:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 12 Dec 2020 17:16:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 12 Dec 2020 17:16:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 17:16:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76813506a5b5f42603d3e7dd21ffcdbc93ecd54b131c1e5ebe9c38e370b3e296`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 13.2 MB (13220305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a4d029641aa49b3d0d084b453a50e8a3e67bff3662df5fc87ffaf20a9066e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad7766cd7aff7822f976c34e812a3092942c547947571e9bdcbd9f68508e93c`  
		Last Modified: Sat, 12 Dec 2020 17:17:06 GMT  
		Size: 36.5 MB (36454568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f908d8fc5d1f1ee55e4dc1f3dc61c4dd732d7f7b83e43b646d53cdd07a89ea`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e98b2139b463dfe7122e7bc9230a3906e7b06ce00968d8cfb231068b02c805`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:156433425592a7b102edd6e991a3322acd7d04cfdb21db0d1953eea604317ada
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103055934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3adf7eb74ed8660fa88d275e6b8ae5b60662457ffdf6e830fec9949d22982f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:05:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 18:05:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:05:53 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 18:06:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 18:06:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 18:06:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 18:06:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 18:06:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 18:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:06:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b64fd1085dc49f926810d3b22f9ad70b1ad5fe33ba9e372ca1655daf1247bc6`  
		Last Modified: Thu, 17 Dec 2020 18:06:22 GMT  
		Size: 13.4 MB (13397499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd7af3576c6b4584d4ddd1b4600001e002c1df436221db37dcd3ce7b116e71`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7075c7442781dddeeecb59ba46407ec9952a85f68e85be98c2fc9dff043d31`  
		Last Modified: Thu, 17 Dec 2020 18:06:48 GMT  
		Size: 34.2 MB (34171997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7772e67accade4d2e117fb4eee1882d4e8f471eb536184fd39f41702fd213d2f`  
		Last Modified: Thu, 17 Dec 2020 18:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3c69945b2cdb0cac65283674bf04677f65dca4bb795a506929e51d4c72820`  
		Last Modified: Thu, 17 Dec 2020 18:06:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9ffe8c25ed921954fde62bc4a0bfec0c2190907ede61c3b61a0abe39421149de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103876557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aba0e826518b3a4d98b627fee9629596b6a2a36e27df40591a4a53282ebded`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:29:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 15:29:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:29:54 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 15:30:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 15:30:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 15:30:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 15:30:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 15:30:05 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 15:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:30:07 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e581a3c8d8ee45a1b2b7bda76c01a7ea09dcf9be92fc9d7a3adfb7ffc785e1`  
		Last Modified: Thu, 17 Dec 2020 15:30:26 GMT  
		Size: 12.9 MB (12926186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3bb5990a1ae62a743fbe010b3203a06825b9dcd10b8de203bf1a7e34d2c8e4`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e973b30c4f0cf4aacec0a19f9a2cab6d297e73687be010c743f08a06c8a89a`  
		Last Modified: Thu, 17 Dec 2020 15:30:47 GMT  
		Size: 34.0 MB (33972728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9868416eec3dbb594a83451e21a6010243dafe9cf25efee6cefc12b946c0`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5c47d84a62bd712e885403834a5f6138dd2e9ac8ce8d7e090098c2f66f9011`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.7`

```console
$ docker pull kapacitor@sha256:0cecb2079c945775ab85c1151089edfcd23799ddae9b4faec568fd62b77f7a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:d3588c0ac35b1ce33e5a1c095092849a0c341be6639f973a0cc97e7d321a9629
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110148872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfb33ff0297a7fbefb06535dcb036b22fadfe69eb48f0aee29352dbc3b8a0e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 17:16:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 12 Dec 2020 17:16:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 17:16:26 GMT
ENV KAPACITOR_VERSION=1.5.7
# Sat, 12 Dec 2020 17:16:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 12 Dec 2020 17:16:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 12 Dec 2020 17:16:30 GMT
EXPOSE 9092
# Sat, 12 Dec 2020 17:16:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 12 Dec 2020 17:16:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 12 Dec 2020 17:16:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 17:16:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76813506a5b5f42603d3e7dd21ffcdbc93ecd54b131c1e5ebe9c38e370b3e296`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 13.2 MB (13220305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a4d029641aa49b3d0d084b453a50e8a3e67bff3662df5fc87ffaf20a9066e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad7766cd7aff7822f976c34e812a3092942c547947571e9bdcbd9f68508e93c`  
		Last Modified: Sat, 12 Dec 2020 17:17:06 GMT  
		Size: 36.5 MB (36454568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f908d8fc5d1f1ee55e4dc1f3dc61c4dd732d7f7b83e43b646d53cdd07a89ea`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e98b2139b463dfe7122e7bc9230a3906e7b06ce00968d8cfb231068b02c805`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.7` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:156433425592a7b102edd6e991a3322acd7d04cfdb21db0d1953eea604317ada
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103055934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3adf7eb74ed8660fa88d275e6b8ae5b60662457ffdf6e830fec9949d22982f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:05:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 18:05:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:05:53 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 18:06:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 18:06:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 18:06:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 18:06:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 18:06:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 18:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:06:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b64fd1085dc49f926810d3b22f9ad70b1ad5fe33ba9e372ca1655daf1247bc6`  
		Last Modified: Thu, 17 Dec 2020 18:06:22 GMT  
		Size: 13.4 MB (13397499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd7af3576c6b4584d4ddd1b4600001e002c1df436221db37dcd3ce7b116e71`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7075c7442781dddeeecb59ba46407ec9952a85f68e85be98c2fc9dff043d31`  
		Last Modified: Thu, 17 Dec 2020 18:06:48 GMT  
		Size: 34.2 MB (34171997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7772e67accade4d2e117fb4eee1882d4e8f471eb536184fd39f41702fd213d2f`  
		Last Modified: Thu, 17 Dec 2020 18:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3c69945b2cdb0cac65283674bf04677f65dca4bb795a506929e51d4c72820`  
		Last Modified: Thu, 17 Dec 2020 18:06:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9ffe8c25ed921954fde62bc4a0bfec0c2190907ede61c3b61a0abe39421149de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103876557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aba0e826518b3a4d98b627fee9629596b6a2a36e27df40591a4a53282ebded`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:29:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 15:29:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:29:54 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 15:30:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 15:30:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 15:30:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 15:30:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 15:30:05 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 15:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:30:07 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e581a3c8d8ee45a1b2b7bda76c01a7ea09dcf9be92fc9d7a3adfb7ffc785e1`  
		Last Modified: Thu, 17 Dec 2020 15:30:26 GMT  
		Size: 12.9 MB (12926186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3bb5990a1ae62a743fbe010b3203a06825b9dcd10b8de203bf1a7e34d2c8e4`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e973b30c4f0cf4aacec0a19f9a2cab6d297e73687be010c743f08a06c8a89a`  
		Last Modified: Thu, 17 Dec 2020 15:30:47 GMT  
		Size: 34.0 MB (33972728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9868416eec3dbb594a83451e21a6010243dafe9cf25efee6cefc12b946c0`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5c47d84a62bd712e885403834a5f6138dd2e9ac8ce8d7e090098c2f66f9011`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.7-alpine`

```console
$ docker pull kapacitor@sha256:c310523c71706fc9c660eb6ef439c7cbed9851f0daefe748940eca510c7f6de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:31dff98f923f839422f76073bb331cb194955b18d29344e824a97274d06001d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23181083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fdee0bdb6b558c7beeadd0ab813f033a4cedbd1a555bae6a39a1d8865492c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:44 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 13:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:48 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:49 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d56cd4d5db30e3deaa9399ca147dd04d20906845467e69ffb63429ddcb90aa4`  
		Last Modified: Thu, 17 Dec 2020 13:24:23 GMT  
		Size: 20.1 MB (20100608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621d1392bc46f51705db0af579d369ebc781d91e0cffe39c32bb15106690586`  
		Last Modified: Thu, 17 Dec 2020 13:24:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583f4e8369224cc6ee0454a49003ec782e76b36fe6ff5a6bdaf820b2110bfb2`  
		Last Modified: Thu, 17 Dec 2020 13:24:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:c310523c71706fc9c660eb6ef439c7cbed9851f0daefe748940eca510c7f6de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:31dff98f923f839422f76073bb331cb194955b18d29344e824a97274d06001d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23181083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fdee0bdb6b558c7beeadd0ab813f033a4cedbd1a555bae6a39a1d8865492c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:44 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 13:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:48 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:49 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d56cd4d5db30e3deaa9399ca147dd04d20906845467e69ffb63429ddcb90aa4`  
		Last Modified: Thu, 17 Dec 2020 13:24:23 GMT  
		Size: 20.1 MB (20100608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621d1392bc46f51705db0af579d369ebc781d91e0cffe39c32bb15106690586`  
		Last Modified: Thu, 17 Dec 2020 13:24:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583f4e8369224cc6ee0454a49003ec782e76b36fe6ff5a6bdaf820b2110bfb2`  
		Last Modified: Thu, 17 Dec 2020 13:24:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:c310523c71706fc9c660eb6ef439c7cbed9851f0daefe748940eca510c7f6de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:31dff98f923f839422f76073bb331cb194955b18d29344e824a97274d06001d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23181083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fdee0bdb6b558c7beeadd0ab813f033a4cedbd1a555bae6a39a1d8865492c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:44 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 13:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:48 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:49 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d56cd4d5db30e3deaa9399ca147dd04d20906845467e69ffb63429ddcb90aa4`  
		Last Modified: Thu, 17 Dec 2020 13:24:23 GMT  
		Size: 20.1 MB (20100608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621d1392bc46f51705db0af579d369ebc781d91e0cffe39c32bb15106690586`  
		Last Modified: Thu, 17 Dec 2020 13:24:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583f4e8369224cc6ee0454a49003ec782e76b36fe6ff5a6bdaf820b2110bfb2`  
		Last Modified: Thu, 17 Dec 2020 13:24:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0cecb2079c945775ab85c1151089edfcd23799ddae9b4faec568fd62b77f7a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:d3588c0ac35b1ce33e5a1c095092849a0c341be6639f973a0cc97e7d321a9629
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110148872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfb33ff0297a7fbefb06535dcb036b22fadfe69eb48f0aee29352dbc3b8a0e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 17:16:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 12 Dec 2020 17:16:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 17:16:26 GMT
ENV KAPACITOR_VERSION=1.5.7
# Sat, 12 Dec 2020 17:16:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 12 Dec 2020 17:16:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 12 Dec 2020 17:16:30 GMT
EXPOSE 9092
# Sat, 12 Dec 2020 17:16:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 12 Dec 2020 17:16:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 12 Dec 2020 17:16:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 17:16:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76813506a5b5f42603d3e7dd21ffcdbc93ecd54b131c1e5ebe9c38e370b3e296`  
		Last Modified: Sat, 12 Dec 2020 17:16:50 GMT  
		Size: 13.2 MB (13220305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a4d029641aa49b3d0d084b453a50e8a3e67bff3662df5fc87ffaf20a9066e`  
		Last Modified: Sat, 12 Dec 2020 17:16:49 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad7766cd7aff7822f976c34e812a3092942c547947571e9bdcbd9f68508e93c`  
		Last Modified: Sat, 12 Dec 2020 17:17:06 GMT  
		Size: 36.5 MB (36454568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f908d8fc5d1f1ee55e4dc1f3dc61c4dd732d7f7b83e43b646d53cdd07a89ea`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e98b2139b463dfe7122e7bc9230a3906e7b06ce00968d8cfb231068b02c805`  
		Last Modified: Sat, 12 Dec 2020 17:17:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:156433425592a7b102edd6e991a3322acd7d04cfdb21db0d1953eea604317ada
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103055934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3adf7eb74ed8660fa88d275e6b8ae5b60662457ffdf6e830fec9949d22982f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:05:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 18:05:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:05:53 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 18:06:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 18:06:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 18:06:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 18:06:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 18:06:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 18:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:06:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b64fd1085dc49f926810d3b22f9ad70b1ad5fe33ba9e372ca1655daf1247bc6`  
		Last Modified: Thu, 17 Dec 2020 18:06:22 GMT  
		Size: 13.4 MB (13397499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd7af3576c6b4584d4ddd1b4600001e002c1df436221db37dcd3ce7b116e71`  
		Last Modified: Thu, 17 Dec 2020 18:06:19 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7075c7442781dddeeecb59ba46407ec9952a85f68e85be98c2fc9dff043d31`  
		Last Modified: Thu, 17 Dec 2020 18:06:48 GMT  
		Size: 34.2 MB (34171997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7772e67accade4d2e117fb4eee1882d4e8f471eb536184fd39f41702fd213d2f`  
		Last Modified: Thu, 17 Dec 2020 18:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3c69945b2cdb0cac65283674bf04677f65dca4bb795a506929e51d4c72820`  
		Last Modified: Thu, 17 Dec 2020 18:06:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9ffe8c25ed921954fde62bc4a0bfec0c2190907ede61c3b61a0abe39421149de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103876557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aba0e826518b3a4d98b627fee9629596b6a2a36e27df40591a4a53282ebded`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:29:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Dec 2020 15:29:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:29:54 GMT
ENV KAPACITOR_VERSION=1.5.7
# Thu, 17 Dec 2020 15:30:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Dec 2020 15:30:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 15:30:02 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 15:30:03 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 15:30:05 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Dec 2020 15:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:30:07 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e581a3c8d8ee45a1b2b7bda76c01a7ea09dcf9be92fc9d7a3adfb7ffc785e1`  
		Last Modified: Thu, 17 Dec 2020 15:30:26 GMT  
		Size: 12.9 MB (12926186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3bb5990a1ae62a743fbe010b3203a06825b9dcd10b8de203bf1a7e34d2c8e4`  
		Last Modified: Thu, 17 Dec 2020 15:30:24 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e973b30c4f0cf4aacec0a19f9a2cab6d297e73687be010c743f08a06c8a89a`  
		Last Modified: Thu, 17 Dec 2020 15:30:47 GMT  
		Size: 34.0 MB (33972728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9868416eec3dbb594a83451e21a6010243dafe9cf25efee6cefc12b946c0`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5c47d84a62bd712e885403834a5f6138dd2e9ac8ce8d7e090098c2f66f9011`  
		Last Modified: Thu, 17 Dec 2020 15:30:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
