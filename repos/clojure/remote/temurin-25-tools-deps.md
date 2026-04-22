## `clojure:temurin-25-tools-deps`

```console
$ docker pull clojure@sha256:226f2c665c4412a39ff2cab0314a1bb06eb9f5a0a874769746c89462c67d5875
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

### `clojure:temurin-25-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:a3a1c41b2b945ccbd8c805034fc8a35e7735d95b7497334691dbb25ecd327fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221912728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94623102554e66c4945571bd9a076208d0b194ed13c25c25bde22c728b449486`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:43 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e37cc7d902a86c38ce1e23e9c33f70d245f7c5e842c46b908b301874ed87b19`  
		Last Modified: Wed, 15 Apr 2026 22:07:19 GMT  
		Size: 92.3 MB (92256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb963a1272479a864153d904470d6dcf0ab55ac772cee9d76bec90cc4dbee5d`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 81.2 MB (81166524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0667f0af2163fe8033aa84019b5f8ca925cfe13bd34e4ad2867d9ff5081e145f`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756d763ecdae7f13cdc633a850d94c2f8a6dddee9233bec9016578824443c874`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:5409cc44d892f44970345a3d435ae6892df57a46976c2546f6692315ca1c6245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8e6899bf762fa6b0b40a6e5da36cb8f16643c8cab6801fb28a12a9feb672fe`

```dockerfile
```

-	Layers:
	-	`sha256:68763c123499ec7ef8ca540990f4499a5fd4d2bd00c25db3878ed72633e5914b`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edfd0d7176ea006f0a7e871520a4db2f24bc6abbf1ef1fcb17cdc8a30675507`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17974e2af9b4cdc02d14960f09a62d70cf549098796436346b36c2c52035f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220836604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a987987c5bbe66a371f0866e5a8c0e3bdc5e597a05dbb3e2b44d846da43cc28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:46 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530464a312d986a46c66e7165a363e2de523dba1bae0690b86e5705e73976613`  
		Last Modified: Wed, 22 Apr 2026 02:24:23 GMT  
		Size: 91.3 MB (91288310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a044efbc47d8383b9a8d4680629c3958b08c7efd97ac8104760b1bc9d073da`  
		Last Modified: Wed, 22 Apr 2026 02:24:23 GMT  
		Size: 81.2 MB (81174184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1214fa3c3d2486af643a010e2b0fa8dadedb922b426f9ba961085bb79298d96`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b157bd29aa34be3f6b9107a8088fc6c6ccc36ec69dbdfd7af5e42a3bf33c85cb`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:6d4e9721cd17e940c60ee01683273d41c100e737387e2da96497acde04f4a5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7027276eb213d6c67e2bee8f8d0db8c54f93ed1cbeba058d96eb9feda96adc1c`

```dockerfile
```

-	Layers:
	-	`sha256:0a1cc2bead94e633a7517462f91a5bfbeab878a068a27832dc1ef9a74b918a20`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abda84debebe17b97bfd91d2c2540c6be2da716ef54ea65aa866da208e233ce`  
		Last Modified: Wed, 22 Apr 2026 02:24:18 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:dfc100757a8adce876845b34fe4c7257317bd54896cb4fe5bd474476bdea8573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230975102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1fe281ebfef406a79359b62ff9ea2366030944347d3bec17ac33a0850e01aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:29:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:29:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:11:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:11:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:11:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:11:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e921237880038077978485833f958f4cb6fe7cf35b55e5d3fcef9da28065c10`  
		Last Modified: Thu, 16 Apr 2026 02:31:28 GMT  
		Size: 91.6 MB (91632998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51ae4194579d5a7161ca1016385ad82b514d8bb814d1515c99d703e3a66556`  
		Last Modified: Thu, 16 Apr 2026 03:12:31 GMT  
		Size: 87.0 MB (87004124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f978be4cbcc00e56bbe3c2e98d4a456156237c9af145daa47cd369d5d5e8f44`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7edfa947d0634de356562012233caad40f84eb678b691aeb636a08647f619`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1371147e8c58c448ce88f78ad6f8faf28056eea76f6667bb04910ae8bf2d2ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b0e15fc1b33c983ae1d458d6871488992d76f4fe97b622508f039086144a4b`

```dockerfile
```

-	Layers:
	-	`sha256:b150287bfec1fab6a4bd65c7ab4b6136ae50db4600f8b1a8ce85f1c3a27c78b5`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59000937e45f9161e1429d94e9e26e806c9a24cdf2545311e789f84e037100e5`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:5fa7b25203fdb1c83e99f92c67906abcc57fc0db137c310d428e8eabd6ef81f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215363103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d3bcd0d52807e7e4cfb0cd9f905b42afeea1d92e896eb7c19db31e6c96e228`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:34:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:34:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:34:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:34:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:34:42 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:44:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:44:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:44:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:44:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:44:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e6a078c5294ff2580dbfaefc5aef8edea3a70059ad98f2fa9ec22eb9d97069`  
		Last Modified: Thu, 16 Apr 2026 00:35:42 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d61f1b92dd89e7abf2412f351b9b6c03912f17e1821cc255bd75a2c96b59e9`  
		Last Modified: Thu, 16 Apr 2026 00:45:26 GMT  
		Size: 80.0 MB (79980141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84578cbea5867baaeed18932c9ff63f8174a26e0d7cb716922e315c74dff2628`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56083f96cbc5c010ec55c2569e81610d48505abeeffc7386cdf638bf25bcf687`  
		Last Modified: Thu, 16 Apr 2026 00:45:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:04e6eb2d44291c6f197c8146d2bedd52ba842a4ed782fe4b9ee7325173adf1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ff4ed37a8fad5e53a4d6956f8b7ee881a7182d0c80a1be73d65872d6b8c115`

```dockerfile
```

-	Layers:
	-	`sha256:64ae8c06cd4365796edc200dbdae466cb32efc2fabd6157ec1bbf40f1fbd01a9`  
		Last Modified: Thu, 16 Apr 2026 00:45:25 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e509d6672bf89147747286bb643159996a6604f9618799f479b902cea1a7faa`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
