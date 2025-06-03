## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:709184b1b0ecf8a006353619c5ca322ead4cbd71b70f4402fae19894400fb1e4
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0ad36b15df885de941217f5f19468beef7ac6112c2b91ee26d5ac267d5dd9974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275118578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74b6da90d16d4414f8858f2ef4b2c7fc7ac545359f473c0aca5c2db0cbdeade`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f5336aba6954dc2fd65c627f000d77fe2cc8c90f3ac9298c32cdf69458005c`  
		Last Modified: Tue, 03 Jun 2025 05:15:46 GMT  
		Size: 145.6 MB (145635587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2e43be8ee8c174c83b3d8f602bcbad98575a6f9a21c333144fbcd59a565777`  
		Last Modified: Tue, 03 Jun 2025 05:15:45 GMT  
		Size: 81.0 MB (80994103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a2667c69665f0a7f8ae392cddc8a8f8502f328c7704268cc9af8b7feb88add`  
		Last Modified: Tue, 03 Jun 2025 05:15:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:728911a8b2eb638edb29f2f0fc8705ce6dd8941bdf99eac4b4a18ebe5e692a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a59f1e7bc3d96ce6b93184b2afe20d4c04c80b556e7433167875b541ad83530`

```dockerfile
```

-	Layers:
	-	`sha256:988da822b76aa537185e13439abfd5330f5fc04b661877ffe37e36e4adee1752`  
		Last Modified: Tue, 03 Jun 2025 05:15:44 GMT  
		Size: 7.2 MB (7238663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204c37f82a9f49bbde0471e0e7ecdebacbac2917e1c752e2dda05288e0d16a94`  
		Last Modified: Tue, 03 Jun 2025 05:15:44 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:229b51ad4d408285dab83e4f29cf2746f1eb4f90be185f97a096c3a0f6d91698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271595211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbaf50ca33ef02fd14b548b4ba6efef78f8cd63d6fc5c4ac0d08c209dc0175a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682800a477954fe07fd9e841558f511dffb10fc0892f35d76669df1d97081e87`  
		Last Modified: Thu, 22 May 2025 08:09:34 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a014d244cc693a83ac405a6d68fbc8e67d1249a0b41af04a62ebe3299ef251`  
		Last Modified: Thu, 22 May 2025 08:14:38 GMT  
		Size: 80.8 MB (80846666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2bd3fdec57256481b3482f92480dfe32b075c2137078d20baa065a0846a68`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:90c327b34bf60ad2cfb5983ce879e31f0bc08451c07eae08161a332f96e0a7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7259414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b845fef0302fe242db6de12b419ba99aebcf70e51714b374d7b087546889304`

```dockerfile
```

-	Layers:
	-	`sha256:69f936ba4cbb6100e62dd5e25828ad68416de89b54b47f720d86f13cc8aa41d9`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 7.2 MB (7245044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c09a6860148eb828829542aa9198fcbe5964840b321015e4c234ac27a5bd374`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0bb7d71ebe28b3ccc796783e6aa5a1ed9177057caa73475ebb83fe943b2d5b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271952911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b494195224503da2ebd8285d7d644e5081d8646a511c9b48b25e2bcaeda21e1a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc84d937b9f9c6a8fdf10268fbf36f3f3530d2d16cd85cb8e98d71c60b41b51`  
		Last Modified: Tue, 03 Jun 2025 08:25:04 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b50880561b0af9251226bc880467d7b00bb4306dc4f8d62fd718475f1f381d1`  
		Last Modified: Tue, 03 Jun 2025 08:35:28 GMT  
		Size: 86.8 MB (86810125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3867edd295aba69a2953eed1a72043ab2d610b31e1d5ecac552727af7e561e1b`  
		Last Modified: Tue, 03 Jun 2025 08:35:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68a061fe837eb635374549bdde9751ccc9d07e907d89bb821ec8093a51e89ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7257552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114693d5cc3edfcd52d9f1fd913bad41aa8f3032fdb8e499c304ae85b81ac807`

```dockerfile
```

-	Layers:
	-	`sha256:2582bd3f70a0f95599aec802b460974a0ccb19a972ba6b637c8b340177531a00`  
		Last Modified: Tue, 03 Jun 2025 08:35:26 GMT  
		Size: 7.2 MB (7243252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d86a550059a9d11d034fbcefda7249158663135be4c42df9b3997741825fce`  
		Last Modified: Tue, 03 Jun 2025 08:35:26 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4eac9df9c9e0d196e66d861cf80955c5b5382629573e7feefd224effb4bc4ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252519730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ce2a57f95eb9e3d696c03079ff637b7c194e11e400da9907a5fcfdc7ccfe67`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c88c5d926257cdcfb8a6708039fa40a0a893499f3bc0262b7011bfd58b087`  
		Last Modified: Tue, 03 Jun 2025 06:00:21 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d530659b7bb106639d8da33cac4d09544c96b6487d31342adece1135559fd`  
		Last Modified: Tue, 03 Jun 2025 06:06:20 GMT  
		Size: 79.8 MB (79789891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300745607ad8c0bd8b44e478cd0f702a159f7d52170521e4624f9ea10ae5b4ff`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:add5c4c21b851f996746d66f23ff79d006b003fa6f5fe2dc08d91530abbb4ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b3c854b308a9e0f805b2444aee7101a3db1af294152fa6513ba6ffbf7cc79`

```dockerfile
```

-	Layers:
	-	`sha256:6142696d3926a54e37dc990fc3485e0d384763758e3d0084d2f15d87b83063f0`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 7.2 MB (7232878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42327518181b085b667584dfbdae006bf5126d0fb6640e472d22d51f8989b79e`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
