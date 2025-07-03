## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:12554d0d8104bc2becf05275c59a7cfe975067be0209ff7d9dc1a3dc35684342
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e391029f56033fb5a045bec17d5a6ad425fb579c780da9e3a98c696febec8dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187716799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e47cba383dcffdd245535b8ede85efc85c02e6bd0195c3ca91bb8722e3f28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3613b7ff44e596289d2b0298e16df1c767af112d9ebb57b914f905eb0830143`  
		Last Modified: Wed, 02 Jul 2025 04:17:43 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b6f9c8ebd41b79cce5ebb6e4dd6858f28b2f80ca379cac1d83edaad5c9084`  
		Last Modified: Wed, 02 Jul 2025 04:17:40 GMT  
		Size: 69.5 MB (69533603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70a8c662d84105f0b8357a59826368fb22517f968d863ab4b122e76341df40`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b833070a83bbe781f33742ff1b46afab7621e9c728b2a13c59614927233351`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b4f41ec2a3331f1d58e8c1081c06303a1629cfd40ad0d8214c0ccd8e9ecd7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca516b45c9b5710d62c92dc7035ebd4b4b771c9620ce8480487a46cefb3f036`

```dockerfile
```

-	Layers:
	-	`sha256:1f25983a7ec3c0f8bc161a441ac4198dc8a79c58c91a5e1fcfb284fba1ad0ee1`  
		Last Modified: Wed, 02 Jul 2025 06:41:05 GMT  
		Size: 5.1 MB (5061890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3909ce15e9446299c9f1e90e2bc8cfa33ca44ee9df7efbcc66310b050ca2c4cd`  
		Last Modified: Wed, 02 Jul 2025 06:41:06 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0cea613bf72590aee22783e7f91a4b7b90183deec2f49e71dad9437e93941c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186558779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874a1791fa27f21c4da03c9c32762f4c203dd34210eea171c1b5188266a54280`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b66ba30c2b454216621d3e6ec97845de73630e952ed659b98479a5cbc4955`  
		Last Modified: Wed, 02 Jul 2025 15:42:34 GMT  
		Size: 89.1 MB (89091278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e3fa61170c970641a4c47e7b00e45644c304b76a4faa404f8d89364b167738`  
		Last Modified: Wed, 02 Jul 2025 13:01:56 GMT  
		Size: 69.4 MB (69388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c58bec72bc17c1dde22ac5ad55acabe524b7a5ee201a965f833ddcf8d712e`  
		Last Modified: Wed, 02 Jul 2025 13:01:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eca9252d60c6d1eb1bf3344afc11da004412bb263aeef171d6e5e575e32e741`  
		Last Modified: Wed, 02 Jul 2025 13:01:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb241834ae07d2fc3063c7e8a4d351c2e7caab562c99395ec2696e797498f006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ff98c9d6303e15985741e6221b5b3b6be07a46745816e371dad5a9ad950bf`

```dockerfile
```

-	Layers:
	-	`sha256:566366380eac81f3eee2e38a7b8f9b29f5001e432b91c6d28c0ae58e3260b30f`  
		Last Modified: Wed, 02 Jul 2025 15:41:54 GMT  
		Size: 5.1 MB (5067648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318a21992e24a8613fc12e6a732f850e8fd05d4f75d06d330c637675288f6d20`  
		Last Modified: Wed, 02 Jul 2025 15:41:55 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:86cae3416ea7c1e8e427f5c91b57eaabe2b1d71f281218c06150443f2175e64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197351325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9363368d74016539267fc680d74b0f18f7a27c7bd5a425b8d8186c7448a99630`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9db4ebf29ca733ca801229ddc796144035d3117992c55d094b94f05f095403`  
		Last Modified: Thu, 03 Jul 2025 13:46:52 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86800c44f1d95322254c8678ee2e319b9559a69805c29193727565eccd94f97c`  
		Last Modified: Wed, 02 Jul 2025 14:12:55 GMT  
		Size: 75.4 MB (75357187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e7007f076d8644f2d739bba522f48ee8dba4897ce2bd814cd69bfaea0e15b`  
		Last Modified: Wed, 02 Jul 2025 14:12:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7290253a04c36ac0db782237fe0a2a041a03b1f913ea4165bd6ac2d824579bbf`  
		Last Modified: Wed, 02 Jul 2025 14:12:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8da87215b87832ab28448dfdd40964e953ea31f0fd8a57bc5f24788ab579f225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669056286e81f75f64bf3a4dbad44d88935890a01a5ea05c3fad1dd1718f0933`

```dockerfile
```

-	Layers:
	-	`sha256:4f336d66a7f60a09e5bb864a28c778cedd19fe759538c3b2a6b6a250fc8d7a57`  
		Last Modified: Wed, 02 Jul 2025 15:42:00 GMT  
		Size: 5.1 MB (5068346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24bb535337587b6fb8eb0c491751d42fb89f2222235ff514126567c74c6a0f`  
		Last Modified: Wed, 02 Jul 2025 15:42:01 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:751899aec45c0fd94f936c490aa63b7b95c95c59231822123c56be81bd82b3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180444263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4763842e28f16c013a917d386f92a7bb47b69ccd9e15c89bc27a21cca8d470b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f04d395d125fbec228c757e4d9d00b68bcdf3d9f3aaba3684b8403802ee00`  
		Last Modified: Wed, 02 Jul 2025 06:57:08 GMT  
		Size: 85.2 MB (85216779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840ace56d51769d4ced2ee3aebd4459b5043cc380030b7934967cd20f7e5119`  
		Last Modified: Wed, 02 Jul 2025 07:01:47 GMT  
		Size: 68.3 MB (68338634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2eaaf828fa5c853d4a247595071f1447c9eb90b0df68e6fda33997784613b`  
		Last Modified: Wed, 02 Jul 2025 07:01:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026ece8fbf4be5d0ea126eb7bc7d72ae7c17863d014aa9d6be1df9698926398`  
		Last Modified: Wed, 02 Jul 2025 07:01:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1449fb1bfc4262e4ea28b4f6acf4e0a328fa8de53197e04cdbe5e4ce9bbe1722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f719a78febe87789c892ae7d1029fa5b4be9876b9c40f543108d29fc838612de`

```dockerfile
```

-	Layers:
	-	`sha256:16fcd9077067486b61a7b4ea8d7e95b76cea66a00e31fceddf679c3b1c448c99`  
		Last Modified: Wed, 02 Jul 2025 09:40:37 GMT  
		Size: 5.1 MB (5055759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c5ec97c8de181ab7dfda9771097ecb94860676c1ea5edac3ea4faf9ad0996e`  
		Last Modified: Wed, 02 Jul 2025 09:40:38 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
