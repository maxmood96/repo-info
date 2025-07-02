## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:f06281f5dc8e9f0a7597ed442d98b87a16c4be38503dd2704fc8b7cd64af6239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:909bf44ff8537c32c74c23f6cc3f0ebaa8ba7186acef6519891b29535ca91b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224572306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36057768c6a68e489f5d16b260aa0ef1b857898dfde5b30ef137b637f3b90a6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8609c9c73f9c388dc1a614c2ece6016f03c02073c3f53602b9ca4bc4cb7741`  
		Last Modified: Wed, 02 Jul 2025 04:17:44 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872adf2c5a575010734881521f0311dd569c6458d592b05994e5e0370f32d43`  
		Last Modified: Wed, 02 Jul 2025 04:17:46 GMT  
		Size: 85.4 MB (85355390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70a8c662d84105f0b8357a59826368fb22517f968d863ab4b122e76341df40`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b833070a83bbe781f33742ff1b46afab7621e9c728b2a13c59614927233351`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d03899f81061e2e434b0bb5c7b0b7e9f5c2135278170a7b1a821f55342566e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9130ae3f28c53070cce4d101daaffaabb68a52dcf88e85be6982557cffb10b43`

```dockerfile
```

-	Layers:
	-	`sha256:5efb9f77c676ace09869c4c909942c702a44cffcb84b26fe537912904258161e`  
		Last Modified: Wed, 02 Jul 2025 06:42:24 GMT  
		Size: 7.4 MB (7409799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59781be4f76544be1099c0309b80933d7f60cc2245d28f679eba1601800e261e`  
		Last Modified: Wed, 02 Jul 2025 06:42:24 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:358c0d393f18ed292017ccf9e4c539549d2a79fbdb2113b5435601262b773860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223894145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8262e9f4e10414044bc8cd75c225ab0e6c7f26e5c7252b1dab1b3fd2df0f57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3201e1aad33692d11acdbc8c155e37cfea431ba1a1deccc85ed3e689d8a5db`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc9769478504162f3979a70a840bb164220e8a93f83fc3c2d8eca5a3471b6bc`  
		Last Modified: Wed, 02 Jul 2025 13:04:32 GMT  
		Size: 85.2 MB (85171728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd51bc75bad532995254635225f397906d7a7884da6d20757830fb046b1d2b6`  
		Last Modified: Wed, 02 Jul 2025 13:04:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554c64c707e662f2e13af1402efd0597587ebb9246aa9495c6e67fe2912bf771`  
		Last Modified: Wed, 02 Jul 2025 13:04:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9bef364d2f2497a59d26e5240fde65b90336b25d1e069e990d73fd98047a1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ebe2c3e4aebfc5bcf746988c7a5e2a0a073cf7f92e2b7e663596182ec69b0e`

```dockerfile
```

-	Layers:
	-	`sha256:5cc763f99151e606df93ad838b603e624d0ea8048d699e0018db287564a0435f`  
		Last Modified: Wed, 02 Jul 2025 15:43:41 GMT  
		Size: 7.4 MB (7416826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06818464d6f9e2054a209ae63094316761aeae887913f8460ddc62aef55afad6`  
		Last Modified: Wed, 02 Jul 2025 15:43:41 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2852fee04589c1d4bae5e6ce8dc76e9742c842de1f014159aca769ca927636ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233787883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e9ff405050dce9a76c48729f7907a3271b7c70470a6d2187e1dfe9c62124f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3bdb985c0e5b4213fe25f1bc15fec160dfdbf3983ad4f63719fbaf61f76363`  
		Last Modified: Wed, 02 Jul 2025 14:07:30 GMT  
		Size: 89.9 MB (89920272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a361e25b445f984e2b8655bd3734d7470f3441e0fccacf8653ea9ac2e2d18e93`  
		Last Modified: Wed, 02 Jul 2025 14:16:13 GMT  
		Size: 90.8 MB (90769332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d350401b4248d99f00ef18bcdc6fcc95bff071aa58f5fc73b566affa40bc71d0`  
		Last Modified: Wed, 02 Jul 2025 14:15:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd88131374dc0b504c39ce153f2302bd18457f91cd7e2a0d886a4596acb24c7`  
		Last Modified: Wed, 02 Jul 2025 14:15:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2270f4bcad975170714fb557ab3069624b4f4baea7969f0e738c537b06a6d7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60bed610ce368c8cb34bf38a52a49ed4c6ecb7a9073c913d678fd711aae4d78`

```dockerfile
```

-	Layers:
	-	`sha256:74764d7ce53fec94d60a77de8af97deebb8ef472beb0ccfd413b23d71d69b3bb`  
		Last Modified: Wed, 02 Jul 2025 15:43:48 GMT  
		Size: 7.4 MB (7415514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea103052a92b60e60c6816f67c966c6862e5ff03cce9f78fdb3817c80020657`  
		Last Modified: Wed, 02 Jul 2025 15:43:49 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:dd516930e73521007ac6135d65d8f98a8b83c9a55f1ef078127d9ce09f2d0541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219611589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac9dcafa4413b69e3eed745f2035fba6365a1be464ff39f79e307c8b1dddce3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f120b17727d388dbdc6b555b4871b73604f60d8e50666c67171b05dec72894dd`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3465929612b1cde352b1dad40f146bcb209704e28a8e5a15548e47be7e2ed7f`  
		Last Modified: Tue, 01 Jul 2025 13:33:29 GMT  
		Size: 84.2 MB (84238227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5cad5cab33ea075270de60c0f480c42b650bb5c9fb772d4bf7b0f6d44815b0`  
		Last Modified: Tue, 01 Jul 2025 03:45:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62b2bd65e2e3cb6614c6281a017aea12a41209fa4a0e6bbf42f3e58681c3d7`  
		Last Modified: Wed, 02 Jul 2025 09:39:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:720791a66c60a6be09ba824371e28a9500750eb5abbf71b16b20e45343ec5131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee4810161e03f9adb336e254ea47e602f1362b33a0dc29713281b69933d6a39`

```dockerfile
```

-	Layers:
	-	`sha256:54e0e9498ebc2d97806922914bcbcabd8a00dab38b0ce1179eb1cb48d1bcb0ee`  
		Last Modified: Wed, 02 Jul 2025 12:41:07 GMT  
		Size: 7.4 MB (7397707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b6ec585c0bbaf78813143d2185bbf375211243008379f545559c060673c774`  
		Last Modified: Wed, 02 Jul 2025 12:41:08 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5c70d02b86d7f604c16daf3adf3ca18193e1b1c3c4e546fa5c043b5d1f3833ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220896274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0f4456dc4221dff0395d16bbd5c9095905d37bdb86ad08f1be53317b885cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc4f9cbbad9b79641e4f5ac67263deac9aa43001430d2662bc7db69f2fcfe7a`  
		Last Modified: Wed, 02 Jul 2025 06:58:54 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7422fc92008076eda4c671d9d3941fa635dada969726d35f2b77a9fa9a3cb1ee`  
		Last Modified: Wed, 02 Jul 2025 07:04:25 GMT  
		Size: 86.3 MB (86334770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707e8a8767b03df22ed062c276194f5ed587ebd1d2e1854fa48b67fa36125d79`  
		Last Modified: Wed, 02 Jul 2025 07:04:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d6ca7601fc34253b635d879d4c11e58480ec9042cea534c6dd4f428d15b9ee`  
		Last Modified: Wed, 02 Jul 2025 07:04:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:68b8ea51bede30ae2831fab1fd3c6d7ddb1af8e0f8c8aebc3df6001d6c11a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7860ee9c0a1611613a2bbb674d951d8e9e8033770b84088ce7853eb29012c`

```dockerfile
```

-	Layers:
	-	`sha256:4a0ea51fcb6c8ceef2fbfa2dda62108dcba47847db8e9b470dff45c00753fb90`  
		Last Modified: Wed, 02 Jul 2025 09:41:44 GMT  
		Size: 7.4 MB (7408269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040e436fafa6a1b8561e0a304c375cef2f14a16bbed0c30da881f283f92e8887`  
		Last Modified: Wed, 02 Jul 2025 09:41:45 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
