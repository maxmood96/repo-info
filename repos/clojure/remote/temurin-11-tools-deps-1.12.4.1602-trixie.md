## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:cdff9f07a88ede4e981d4d4c7ef3977a9d2c30234cde644c9e7d028003eaa749
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:67a459b3e90fd7b353b26612d43f96956af69c6659f7245584286933fadfaa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279802662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e21857e4e0635567d3e457aa3dd924b18c06af79178d6beea049ad43128150`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:49 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586c2f1503a6927150a2ecd56e4ee9a21f3aa9eaceb74f6739b344505adc89ed`  
		Last Modified: Tue, 03 Feb 2026 03:20:31 GMT  
		Size: 145.0 MB (144966607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d2357d95b9beacaf322ba96abc027eb13694522ebed33beb700f77fa534a7`  
		Last Modified: Tue, 03 Feb 2026 03:20:30 GMT  
		Size: 85.5 MB (85542456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2846665d4480ca5a4551a5fa4e1c28c6961661c994c108c34af6fa0a0c1f91e`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b93bba7f4142ab76a1051237bb79da3d860e171022e60176716dd88862d4c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b8568746c86af65cbca0200859fd5a2846a9364670a99b27b46ac5f364ec52`

```dockerfile
```

-	Layers:
	-	`sha256:655892149e0eee83f4eb975bfec0a0d98784e46b70c888fe1fa44c203b4fdedc`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 7.5 MB (7487967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6855ad01cf65b56801797b45af6b3761d20fa0f56705506b3b2ef774e76fa2`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8aba6e34f0f94cd7a83407afaf7b014bc60f62c2b78b34d2f9aa1031629fb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276743743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c73bbe0bf421c0f3cf954284d421ad117c92acce7557a3f7fe1d018e8f15b7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:24 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c0bbf6cb91a6aca274791498a4f3f1294e4071d6ea4df96a407abdd260af3`  
		Last Modified: Tue, 03 Feb 2026 03:23:04 GMT  
		Size: 141.7 MB (141729907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53faabd019a77daa1df57be55e151deb72fb5f85253a8b5c40c65b1e0c576f03`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 85.4 MB (85361170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bfbccf1730f5a749c6b654d76f3d0eb7ef27a494b6018ddff67ddb5db2e2ba`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:124601bdbf2ea731aaec8bad0c2052b17ffd438ff58f03e43a2ffe8875ff08b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b7bd1a6ef87a2e60f8e22204596dc873d00407f822e028b68e661ff39c2fd`

```dockerfile
```

-	Layers:
	-	`sha256:8a8ae27f9e0e19ccc05fc3653daa25e195e8e47d5081a2d263dd88291334c91e`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 7.5 MB (7495615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f7adc3334bd489cb0dd57c23bdb782359aa2d4c9d6c38b7db479896259fb91`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b89a793126e3696491edc5dad3e2757745451e602636acb938351c1808f28a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276139558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2558649f3b07b5d2de9b1ffab9c09302326906142094f11c8c1ab4e111570621`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:35:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:35:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:35:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:35:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:35:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:39:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:39:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:39:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d550e8e3e84307a53a865255ffa7934eb6a2d4a27cf9304f480d6e6b94183b`  
		Last Modified: Tue, 03 Feb 2026 09:36:41 GMT  
		Size: 132.1 MB (132079737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0bfb24d3b1debd21b590c7f5b72d210e79277fef320ce7e3100e4138899e4d`  
		Last Modified: Tue, 03 Feb 2026 09:39:53 GMT  
		Size: 90.9 MB (90947060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ca7ce7192d6533aa056308e56727e2c161e16ade64792ff689a48021612bf4`  
		Last Modified: Tue, 03 Feb 2026 09:39:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:78616da9e761ab3e25980d14a9c8cb52c09b441c896b8711573c71894e167ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cbfbc98d652718ebb5c6fb65022518e2b2211f68dba3042ee1a5281659d7fb`

```dockerfile
```

-	Layers:
	-	`sha256:af27b77c8757bfeb955d1774ee7d3cc8edf0ea10fb90502d0b973df541756167`  
		Last Modified: Tue, 03 Feb 2026 09:39:51 GMT  
		Size: 7.5 MB (7491773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6e33ed341d68bea7729ed3f7e9d21fc0b0b73193a9aea41ee40872935bd2f2`  
		Last Modified: Tue, 03 Feb 2026 09:39:50 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b40a6a1195636ab1dd35b72253d3b618bfcce1c484d28413e9dcf604c62bb8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261561436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7210fcd52a96e43c259fb143028282c3342cd42a5db6a386cc4962826803b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 04:59:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:01:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:01:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:01:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79570d0434267dfc1c3c1e2bf2c0aeed5bd16edce07420e924b763e62dc668`  
		Last Modified: Tue, 03 Feb 2026 05:00:38 GMT  
		Size: 125.7 MB (125694888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872e8367e9e81779b16552aa60831f777ea79b60444fb24816c52fcc9aa56d9`  
		Last Modified: Tue, 03 Feb 2026 05:01:42 GMT  
		Size: 86.5 MB (86511524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c8371eae7f7afb748510853405af12fba13516ca06149506dadcd6939faf56`  
		Last Modified: Tue, 03 Feb 2026 05:01:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5349994553170b0f98c2fa4eef4869cfedefe0067812e0c09f2d1a9b84800ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ad01efc54b1ceab1a0f8a5857a1bb01cc16132cbd5f446019abdf789b2dabc`

```dockerfile
```

-	Layers:
	-	`sha256:7f9795c3811359d8bf9e2e35fa9cd3206d1710ea731cfa15d805c93bd42af3e9`  
		Last Modified: Tue, 03 Feb 2026 05:01:41 GMT  
		Size: 7.5 MB (7483893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2931f12f56f46bcc053ca620f641eb1204121237255e95dc9e95b15b0524eba4`  
		Last Modified: Tue, 03 Feb 2026 05:01:40 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
