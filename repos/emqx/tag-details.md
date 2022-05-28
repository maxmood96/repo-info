<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.5`](#emqx435)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.3`](#emqx443)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:232f8b880d878ff3146bef1eee6bc2d04687fbcbdf5592a67d1d5bba55cd96a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:4cb1b0bb8ae82b9cb24070637c1905bdbbe7921c5ea6f5fb13c28c2713a5bc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124757921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75f6418039300da26c9db971a8e7178237250a17e8426713fba15284cab2a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:49 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 02:10:49 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 02:10:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 02:10:59 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
USER emqx
# Wed, 11 May 2022 02:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 02:11:00 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 02:11:00 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 02:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 02:11:00 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd6307b042fcd9f6285a63a7a406062b071366c22ac1f023c12bd724cce11`  
		Last Modified: Wed, 11 May 2022 02:11:27 GMT  
		Size: 2.6 MB (2568166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8eabbb9a2020c7a0789a591f11ac886c99b729505bc1659a8c9331ca82686`  
		Last Modified: Wed, 11 May 2022 02:11:31 GMT  
		Size: 45.4 MB (45398067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c485e76e7ea9a5005f3abccf0a2645a0e49ff79b5f058ba5964c5b5a93dfa2`  
		Last Modified: Wed, 11 May 2022 02:11:32 GMT  
		Size: 45.4 MB (45411105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd216f270eba6422d39d7df904f31c35207069917fc19a59a22b0f4803e0fbab`  
		Last Modified: Wed, 11 May 2022 02:11:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:821e65c41f85afdf4bebc5235506f954c5a1f620a0a972389b6c73d62e5d6319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:d215b64bdd117916b9cfc94ed9be9b9ab30ed417e93be36daa3c7f840264c924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62027585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac57bff3f84138cf3e7c10bec3c32f22673e11ba0056df747f11ff013be6e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:01:22 GMT
RUN groupadd -r -g 1000 emqx && useradd -r -m -u 1000 -g emqx emqx
# Sat, 28 May 2022 03:01:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates curl gnupg;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:01:31 GMT
RUN set -eu;     key='FC841BA637755CA8487B1E3CC0B409463E640D53';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";     mkdir -p /etc/apt/keyrings;     gpg --batch --export "$key" > /etc/apt/keyrings/emqx.gpg;     gpgconf --kill all;     rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 03:01:31 GMT
ENV EMQX_VERSION=4.3.5
# Sat, 28 May 2022 03:01:45 GMT
RUN set -eu;     echo "deb [signed-by=/etc/apt/keyrings/emqx.gpg] https://repos.emqx.io/emqx-ce/deb/debian/ ./buster stable" >> /etc/apt/sources.list.d/emqx.list;     apt-get update;     apt-get install -y --no-install-recommends emqx="$EMQX_VERSION";     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:01:45 GMT
USER emqx
# Sat, 28 May 2022 03:01:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 28 May 2022 03:01:45 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 28 May 2022 03:01:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:01:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e2af97cab2a12889006fbc43195c94b3b40e2f709a67638127d4743eba1b64`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db304b4b83a187dcc3cf815976fc7b1b9fd2329f766cb60f7dcee25dcbb434`  
		Last Modified: Sat, 28 May 2022 03:02:16 GMT  
		Size: 8.1 MB (8141789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301386ecf8894cc04539f444c679471a47c60c05a31e7a5fef0a4cc9138a938`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1645e3f3d4a2d1962fa930b72671692758f82fbe58383f31c79f3ae94b9987`  
		Last Modified: Sat, 28 May 2022 03:02:18 GMT  
		Size: 26.7 MB (26739631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636b002f692258f32ff33fe5c3a68a3de4c1c21e9e1a43031df76a73341f36e1`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.5`

```console
$ docker pull emqx@sha256:821e65c41f85afdf4bebc5235506f954c5a1f620a0a972389b6c73d62e5d6319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3.5` - linux; amd64

```console
$ docker pull emqx@sha256:d215b64bdd117916b9cfc94ed9be9b9ab30ed417e93be36daa3c7f840264c924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62027585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac57bff3f84138cf3e7c10bec3c32f22673e11ba0056df747f11ff013be6e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:01:22 GMT
RUN groupadd -r -g 1000 emqx && useradd -r -m -u 1000 -g emqx emqx
# Sat, 28 May 2022 03:01:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates curl gnupg;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:01:31 GMT
RUN set -eu;     key='FC841BA637755CA8487B1E3CC0B409463E640D53';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";     mkdir -p /etc/apt/keyrings;     gpg --batch --export "$key" > /etc/apt/keyrings/emqx.gpg;     gpgconf --kill all;     rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 03:01:31 GMT
ENV EMQX_VERSION=4.3.5
# Sat, 28 May 2022 03:01:45 GMT
RUN set -eu;     echo "deb [signed-by=/etc/apt/keyrings/emqx.gpg] https://repos.emqx.io/emqx-ce/deb/debian/ ./buster stable" >> /etc/apt/sources.list.d/emqx.list;     apt-get update;     apt-get install -y --no-install-recommends emqx="$EMQX_VERSION";     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:01:45 GMT
USER emqx
# Sat, 28 May 2022 03:01:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 28 May 2022 03:01:45 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 28 May 2022 03:01:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:01:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e2af97cab2a12889006fbc43195c94b3b40e2f709a67638127d4743eba1b64`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db304b4b83a187dcc3cf815976fc7b1b9fd2329f766cb60f7dcee25dcbb434`  
		Last Modified: Sat, 28 May 2022 03:02:16 GMT  
		Size: 8.1 MB (8141789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301386ecf8894cc04539f444c679471a47c60c05a31e7a5fef0a4cc9138a938`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1645e3f3d4a2d1962fa930b72671692758f82fbe58383f31c79f3ae94b9987`  
		Last Modified: Sat, 28 May 2022 03:02:18 GMT  
		Size: 26.7 MB (26739631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636b002f692258f32ff33fe5c3a68a3de4c1c21e9e1a43031df76a73341f36e1`  
		Last Modified: Sat, 28 May 2022 03:02:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:232f8b880d878ff3146bef1eee6bc2d04687fbcbdf5592a67d1d5bba55cd96a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:4cb1b0bb8ae82b9cb24070637c1905bdbbe7921c5ea6f5fb13c28c2713a5bc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124757921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75f6418039300da26c9db971a8e7178237250a17e8426713fba15284cab2a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:49 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 02:10:49 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 02:10:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 02:10:59 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
USER emqx
# Wed, 11 May 2022 02:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 02:11:00 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 02:11:00 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 02:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 02:11:00 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd6307b042fcd9f6285a63a7a406062b071366c22ac1f023c12bd724cce11`  
		Last Modified: Wed, 11 May 2022 02:11:27 GMT  
		Size: 2.6 MB (2568166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8eabbb9a2020c7a0789a591f11ac886c99b729505bc1659a8c9331ca82686`  
		Last Modified: Wed, 11 May 2022 02:11:31 GMT  
		Size: 45.4 MB (45398067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c485e76e7ea9a5005f3abccf0a2645a0e49ff79b5f058ba5964c5b5a93dfa2`  
		Last Modified: Wed, 11 May 2022 02:11:32 GMT  
		Size: 45.4 MB (45411105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd216f270eba6422d39d7df904f31c35207069917fc19a59a22b0f4803e0fbab`  
		Last Modified: Wed, 11 May 2022 02:11:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.3`

```console
$ docker pull emqx@sha256:232f8b880d878ff3146bef1eee6bc2d04687fbcbdf5592a67d1d5bba55cd96a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.3` - linux; amd64

```console
$ docker pull emqx@sha256:4cb1b0bb8ae82b9cb24070637c1905bdbbe7921c5ea6f5fb13c28c2713a5bc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124757921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75f6418039300da26c9db971a8e7178237250a17e8426713fba15284cab2a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:49 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 02:10:49 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 02:10:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 02:10:59 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
USER emqx
# Wed, 11 May 2022 02:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 02:11:00 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 02:11:00 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 02:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 02:11:00 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd6307b042fcd9f6285a63a7a406062b071366c22ac1f023c12bd724cce11`  
		Last Modified: Wed, 11 May 2022 02:11:27 GMT  
		Size: 2.6 MB (2568166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8eabbb9a2020c7a0789a591f11ac886c99b729505bc1659a8c9331ca82686`  
		Last Modified: Wed, 11 May 2022 02:11:31 GMT  
		Size: 45.4 MB (45398067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c485e76e7ea9a5005f3abccf0a2645a0e49ff79b5f058ba5964c5b5a93dfa2`  
		Last Modified: Wed, 11 May 2022 02:11:32 GMT  
		Size: 45.4 MB (45411105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd216f270eba6422d39d7df904f31c35207069917fc19a59a22b0f4803e0fbab`  
		Last Modified: Wed, 11 May 2022 02:11:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:232f8b880d878ff3146bef1eee6bc2d04687fbcbdf5592a67d1d5bba55cd96a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:4cb1b0bb8ae82b9cb24070637c1905bdbbe7921c5ea6f5fb13c28c2713a5bc92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124757921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75f6418039300da26c9db971a8e7178237250a17e8426713fba15284cab2a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:10:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:49 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 02:10:49 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 02:10:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 02:10:59 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 02:11:00 GMT
USER emqx
# Wed, 11 May 2022 02:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 02:11:00 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 02:11:00 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 02:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 02:11:00 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd6307b042fcd9f6285a63a7a406062b071366c22ac1f023c12bd724cce11`  
		Last Modified: Wed, 11 May 2022 02:11:27 GMT  
		Size: 2.6 MB (2568166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8eabbb9a2020c7a0789a591f11ac886c99b729505bc1659a8c9331ca82686`  
		Last Modified: Wed, 11 May 2022 02:11:31 GMT  
		Size: 45.4 MB (45398067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c485e76e7ea9a5005f3abccf0a2645a0e49ff79b5f058ba5964c5b5a93dfa2`  
		Last Modified: Wed, 11 May 2022 02:11:32 GMT  
		Size: 45.4 MB (45411105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd216f270eba6422d39d7df904f31c35207069917fc19a59a22b0f4803e0fbab`  
		Last Modified: Wed, 11 May 2022 02:11:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
