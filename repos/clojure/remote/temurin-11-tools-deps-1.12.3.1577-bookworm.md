## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:90d7e7f813771a00752e3ac56a99c9e2b33ee6bb41adac6b558a0b286db5cdfd
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bdc0f9ee88cc199ac453b5880c6a639d1bdc632207c3e7e2b6f08e523da807ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274594581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8e12c41ba788d9539c75f1152d06462586042ffbe0a13d5ed14b06c9baa162`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:28 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754c3be208966e18eb048cc2740b60a03a00d29cb9d8a06f12ed21c065290c9c`  
		Last Modified: Fri, 14 Nov 2025 00:52:06 GMT  
		Size: 145.0 MB (144966606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf361e77fe641d7ee3381cd21d611e52dd14ac917554a9592ec9018d4319de49`  
		Last Modified: Fri, 14 Nov 2025 00:52:17 GMT  
		Size: 81.1 MB (81146274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bea0671effa9d99d43a73ecce560ccbff12fd98fca257df988f10ee64a7ce5`  
		Last Modified: Fri, 14 Nov 2025 00:52:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3407320f94611daa089a41cedba0570c1dfc52dd5cfd32967868ff1d183fd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f21c2c41d7132c8932b0263c8332671a3178820657b8e281acd6991d1d7e6`

```dockerfile
```

-	Layers:
	-	`sha256:281e0a2f6557664bf8b15f440656af5dc384089258fd48efeea61b24b9873ba2`  
		Last Modified: Fri, 14 Nov 2025 04:35:12 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee145afcf4cc91d3861a5cf31d9547a5d9862d064fb73948b864158365298d4a`  
		Last Modified: Fri, 14 Nov 2025 04:35:13 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d9c37ff87677aa7b5ae815ff4a543f44208e10f57b81700bd15e89d61c1adad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271122745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e50dd77f1990c8ec1d9879e604c32f3a8964258ee312dabec33015233d24e1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:00 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae77eabf1dfd34ba398e5fe96b1258bb6907545f07036cb57288478c07639d6`  
		Last Modified: Fri, 14 Nov 2025 00:53:40 GMT  
		Size: 141.7 MB (141731559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa0985b4991f20fce24bfa989df4416c33ae9579a2d4b5cb695ced130d65d7f`  
		Last Modified: Fri, 14 Nov 2025 00:53:52 GMT  
		Size: 81.0 MB (81031062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e6f58aa50aae2902052bfa78110974fca0b920a3fc1ed3c97e47922ec026d`  
		Last Modified: Fri, 14 Nov 2025 00:53:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:19e27dd84f63f299217813a70fe3d5be9490d698d2013d69d29ec024695629e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045ef5823fd8eb7c6720d2246b8053916eb932a712123908d410d7a2779a80e4`

```dockerfile
```

-	Layers:
	-	`sha256:3f4788d4db118649e190a4076d8a1708b635469e29f12c812bdf5f7c8ba21522`  
		Last Modified: Fri, 14 Nov 2025 04:35:18 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36d2070b822af514898e1c874816ea72e6bfa11290ebc4fa2b5526db46668cb`  
		Last Modified: Fri, 14 Nov 2025 04:35:19 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:585cbb09c745596c39c5335b802be67742c85cbe536ebdff9c84c5eb7ad98c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271396336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959b6e5f629a45ec90f6f927b04372a8717d2e4d0edd08158ba61ebac3f7da58`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 06:41:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:41:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:41:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:41:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:41:41 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:50:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:50:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:50:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238de4ff071f95dde9440cdd15af8c8880cccce0f7ad181edeb4d583736ea938`  
		Last Modified: Fri, 14 Nov 2025 06:42:55 GMT  
		Size: 132.1 MB (132081994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf22a7a24ed84cb8d74c392de0c9c96bcda92e292d0fa59357e127fb63e572f`  
		Last Modified: Fri, 14 Nov 2025 06:51:11 GMT  
		Size: 87.0 MB (86986418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7223f30c66ca6850f293bfa2bd2701a2b323e0a7fd2eaadeb905af590cefe1`  
		Last Modified: Fri, 14 Nov 2025 06:51:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dcafd500c2a11f01a92be8c47e1a4c7d9553a1a6270f38186c894f71448e9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007f6064f566389d03c72b84aa8ffb265d124fae4eb0beff3ae2d2b86126b68`

```dockerfile
```

-	Layers:
	-	`sha256:f3698d01fc7d00f5d29e22cdc8608c4968961a8cc65a7aa373f9bb50905b5fa5`  
		Last Modified: Fri, 14 Nov 2025 07:34:47 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d11cbc6264ee9c1e6b35e91dcd9a83243c72e01ca1fc66b9706cc59acaae73`  
		Last Modified: Fri, 14 Nov 2025 07:34:48 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e2621710b797ec4746cf7822fe021a866d02198673c39dca6f8dab5b4d2290c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252789893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458b5ffc7e63c1754797336a5086b57edf76c2e95d6f1c5dd5baf9d29df51aa2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:02 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbe8f4a4af229f68604f530b54b1a629a4763adde262720b5a0979ad57d6b30`  
		Last Modified: Fri, 14 Nov 2025 00:54:04 GMT  
		Size: 125.7 MB (125694442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f29c369d48c5bd7a02a1fba0ebb501993ea32c6c64d2cfc0c897ea3b00776`  
		Last Modified: Fri, 14 Nov 2025 00:53:56 GMT  
		Size: 80.0 MB (79956713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc87ba347448543574bf4923767cc7214148f3a2705270d3e3ff0d9213d87dd6`  
		Last Modified: Fri, 14 Nov 2025 00:53:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c60fd015897f22abef30a110f042a3a639bcf49df2786598e5d6b1d63a2a295f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3f29f22843b3788a9af547f8c2fdddd58960db122f8a73c951c88244fac36`

```dockerfile
```

-	Layers:
	-	`sha256:9fd49b62e9f3e541cd8da77283e351308aafacb1acfd178ec16ea79737939299`  
		Last Modified: Fri, 14 Nov 2025 01:35:38 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4156eb8fb57bc214fba313cea4e17d75898e3ee15f1119523c24b4903b263656`  
		Last Modified: Fri, 14 Nov 2025 01:35:39 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
