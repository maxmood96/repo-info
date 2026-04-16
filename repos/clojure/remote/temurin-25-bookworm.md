## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:285a0ff49da736296b9d7821643046cf1ed23f72890238c115c53d461919fa56
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

### `clojure:temurin-25-bookworm` - linux; amd64

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

### `clojure:temurin-25-bookworm` - unknown; unknown

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

### `clojure:temurin-25-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:858314769031818754a3f23310ec1bd9a3e5491f7c5adb3f61e0ae7dcf808972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220834254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fd434e0f8b9ebe39e429299952c81dfea1cf84d699c0ff9cf09afd1e0e3e2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ea87d9db184f50636c17f919ecba69b68925c4fdb88e4d7b1cbba1603fb02e`  
		Last Modified: Wed, 15 Apr 2026 22:18:55 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beb79696d2dd98a3ff54f892774a9154733017e11bec6cbed2482d155312df8`  
		Last Modified: Wed, 15 Apr 2026 22:18:55 GMT  
		Size: 81.2 MB (81171684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb45b7c17225a32d3dfdeeba60735bc10b731db9c16e87bba3ca40963ad9d9d`  
		Last Modified: Wed, 15 Apr 2026 22:18:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0bd0e3a90544e6126f2eb7d2e043c482465833ded1bc6fe6821e738b6b85`  
		Last Modified: Wed, 15 Apr 2026 22:18:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:aed77d13777eb60ee739b4dce4168b7c3c5ca41a8ce1cbe8b3ca71469b913f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef42ef317ec6496116701f38e6efaa4e7c2d91c775be9d17a927e659583ed2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1166500fb6ff405e0438e6426c7b399ea78edd1e459b084ceca15c877025cf`  
		Last Modified: Wed, 15 Apr 2026 22:18:52 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75781f778eb5468de87ce4378daa79d6706043a1d391d2c6329d8febb302854`  
		Last Modified: Wed, 15 Apr 2026 22:18:51 GMT  
		Size: 18.0 KB (17960 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; ppc64le

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

### `clojure:temurin-25-bookworm` - unknown; unknown

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

### `clojure:temurin-25-bookworm` - linux; s390x

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

### `clojure:temurin-25-bookworm` - unknown; unknown

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
