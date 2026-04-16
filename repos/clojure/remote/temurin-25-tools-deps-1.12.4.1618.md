## `clojure:temurin-25-tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:20765579c1d341e2f1902867488ffc426a0c7715fe098332f87730149fedb0a8
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

### `clojure:temurin-25-tools-deps-1.12.4.1618` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.4.1618` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c904cfa4a2cb4fd93326c165b80fcba78038e678c38532841404a788d2b87d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220821052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54281b990739cde81dc6bf24a36d095d71e5fe22ac2b2cf21000c6c08431292a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:28:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d07c0a2b3ea68a2e73df43a2e01a5d7ac24c6101d398d9cf49237658a2f4b5`  
		Last Modified: Tue, 07 Apr 2026 03:28:40 GMT  
		Size: 91.3 MB (91288283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60917d6a521e9cf71ad41d3ceec0a002a94d83fa277692c0f3f851b97531739d`  
		Last Modified: Tue, 07 Apr 2026 03:28:39 GMT  
		Size: 81.2 MB (81158465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc107aa34e2912f396f00ff01e40512b79436d5f676c22263fefe133fff75f14`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f1410944bc2cb8d36ed0d8b16aa3d3beb4109ae5235b6b3525dfa16f63a86`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:8d493a433b9b20a9ee84f561b58cc4944eda72231734986fb2ed8d31be157459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8281aa6e95b3fc4ed950919ae771b92710e33347cd1ea84ec2b23e902642a8aa`

```dockerfile
```

-	Layers:
	-	`sha256:26ad2bc1a40991faeccfd93f311ca8b3cfebe32eec75cc3761b158df7fabbba0`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cdb5d0238ef3d94e827f4dca00486a07011440c468fd4085008faddad4e9df`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 18.0 KB (17960 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:b8d206f17909e4595ad803bc1b4dfad861c30261cd04ace6cfd1c4296cfa8c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230971299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540b9c99d6142ff3b9330de38cecf5d43b4bb7bbcd60b6821686071a7c2d2f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:18:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:18:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:18:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:18:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:59:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:59:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:59:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:59:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:59:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37828c75dd85ae1dfea53ab4854b6b0d30152c9a1fa77b22f23ecfe7b3ca4a`  
		Last Modified: Tue, 07 Apr 2026 14:21:10 GMT  
		Size: 91.6 MB (91633006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37bffea90a7eb00b6d52d3a71b2934882a16243bf8c35a89bbd73c6ffdb8474`  
		Last Modified: Tue, 07 Apr 2026 15:00:11 GMT  
		Size: 87.0 MB (87000315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed13b1adcd4797b2e41714eea3f82b46d21d5ffd7214f2782f3d6f60ccc9fd7`  
		Last Modified: Tue, 07 Apr 2026 15:00:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2786cc741f0962aefe00280c2a67fe79c6af73825164a4ccdae6adf202e9c1`  
		Last Modified: Tue, 07 Apr 2026 15:00:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:3e2d3978ef8d7e354898ca82bd468d3031560f5451531944f167701c94c9db59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0e2c11a5b826c0d7954a57ea3a304d4deb018f49160b21e339a43294b2d999`

```dockerfile
```

-	Layers:
	-	`sha256:d63799f968d104abf03d0ba78b18363393f5f2fe779193095d3025f3af60eae2`  
		Last Modified: Tue, 07 Apr 2026 15:00:10 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ce7293706a5b13a0177244d91ddaf355b54fcd0c81409b7e8113b649609a1b`  
		Last Modified: Tue, 07 Apr 2026 15:00:08 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:3e790ca5dfef22f9954ad9c14b981b59cde1d79f39ed16ae79d5bae47f0f6d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215371196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ce0b11a546eace065a63bb0fefa7b10b16cbcb08c836bc15fd58a802f79932`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:38:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:38:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:38:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:38:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6336049cfea2fb1bf6fe937dfa06a3231de1bcd109cc0d07cc3ba41fd378402`  
		Last Modified: Tue, 07 Apr 2026 05:39:45 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b094f534efd8875b5477a6fbceb9e28bf6c0aaf1f360120e57b42a374bd333`  
		Last Modified: Tue, 07 Apr 2026 05:48:20 GMT  
		Size: 80.0 MB (79988269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93f4f66b08c3531a0b733e6d5d0b043c755b95ac93594bb90d5b1b3a091991`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a4e31486c7492ded9784d6539d8cd4c90163a9f7c831ba535d83bc09d966b5`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:46473c221197a049a7cf545472b649787b01bfb085b3394c75d3cf6c38d1ab78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68637d68b86e502b64513b03449da35429ae68fce94b19c4f3585bfd682c6d83`

```dockerfile
```

-	Layers:
	-	`sha256:c0cf42260a90b9c04c08951d623a01345d912da4f0132eb61808a282069b0d1f`  
		Last Modified: Tue, 07 Apr 2026 05:48:19 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b39cbadbe24091c5dbc8e92f4805ead7eaf94b04d8d3038f121d61dbacc8a8bf`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
