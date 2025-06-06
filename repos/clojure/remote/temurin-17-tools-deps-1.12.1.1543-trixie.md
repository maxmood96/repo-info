## `clojure:temurin-17-tools-deps-1.12.1.1543-trixie`

```console
$ docker pull clojure@sha256:a56ae93a520ccc674c81404226bd423681837512da1dba765270990d6576b70a
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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2c590f14a456b6a8c2e81266776e8ecc7b448147b1ce589e5f5dcad201089c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282090242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d857b82c8416a9522e18af0ef28e4637143cf6f3973d6b54b68c27f07461dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652fe390832cb451f9074a7189cf88400e116c8ba451214832baa5e31766848`  
		Last Modified: Thu, 05 Jun 2025 03:33:10 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8887d46d4c457b3de3c70374cb1829b1c74185f3f7ad16c886601c3ef469b2`  
		Last Modified: Wed, 04 Jun 2025 06:23:51 GMT  
		Size: 88.2 MB (88207266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6868198e736cb248f1e199fa05387c5c07fe0e979b49218e365dd7f853d1f7f9`  
		Last Modified: Tue, 03 Jun 2025 18:29:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8085542e21368352560de3fd15327a82e4de61a526a17454642cf8866cec1a15`  
		Last Modified: Tue, 03 Jun 2025 18:29:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:69ac090aa9f9fca2eb01b370e45bf8ec900f856fa708e5650905d8e79c8b61bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c1f642257f76fc17503da42a69a5829c76ed4061b529a9ae2722475649c293`

```dockerfile
```

-	Layers:
	-	`sha256:fcb1366c675dc3a0c96a60e4f1cc3aaa5ef63a11585f4d3cc37574e913130f38`  
		Last Modified: Tue, 03 Jun 2025 21:38:56 GMT  
		Size: 7.3 MB (7318416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7971d55e78fb76f6b81cf1855146bc5ce0929b9c6444185ae27c0f1824c15013`  
		Last Modified: Tue, 03 Jun 2025 21:38:57 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27bf9ee39b3e6a3fd905f0a7c6b87869f7667ce57f8f409eded0e1c979bf0a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281643323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36354f0924d2a1cc3bf2fe1bd128390aaba29a2b5f477cd900ba0e14d3e98825`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Fri, 06 Jun 2025 12:50:12 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7ed68d0038da0d50dee33322553005f427b2497ee2df92baf02932c001f6c`  
		Last Modified: Tue, 03 Jun 2025 18:43:42 GMT  
		Size: 88.5 MB (88511364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f265aa80e8753e393b6e9dd9f0a5972d392120452474f8144c33782d29925`  
		Last Modified: Tue, 03 Jun 2025 18:43:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5eb8c29601e726fb9c3590ae674be1b6d6833862f14c5ab1f35c0997b0c213`  
		Last Modified: Tue, 03 Jun 2025 18:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e523d1a0e36da4fc8a5cceede76cbf5063067635ebd571a882992886ae705fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d0cc545ae89b3827419c2c48064b74c030a09f7efe473686e0c8c2e7c39842`

```dockerfile
```

-	Layers:
	-	`sha256:0e06e7ec307fb562886f0b468316cbbb6a74e2cc1c098ee52a67ce25ec419300`  
		Last Modified: Tue, 03 Jun 2025 21:39:02 GMT  
		Size: 7.3 MB (7325446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7586fee26c25791db8d2b74fe16f26e0b613b08198f186cb265dac7371dd445`  
		Last Modified: Tue, 03 Jun 2025 21:39:05 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2467a004315f7c909c684af056b24db73736ac07f0c84df80b6881286b15289d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291312402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe38cde0845026a49521278f7fd1b6ff9e7db3937ca9427d085805b8e0b3a7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 03 Jun 2025 08:51:10 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378d026768dc7112a489469dade2d6b8098e6b9a51e805e66e2e83c3a3a4d1cf`  
		Last Modified: Tue, 03 Jun 2025 18:56:04 GMT  
		Size: 94.0 MB (93950231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a829ef5615b502753351f7118504464780eaaebfcada66d3a90ce9712d935cc`  
		Last Modified: Tue, 03 Jun 2025 18:55:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1646688320cb2a910b38aded6bce9d3e826e0379ed3cbd69d7f1eba29d10cb0`  
		Last Modified: Tue, 03 Jun 2025 18:55:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a9febcf8f0258b79a74a80f5962360a90fc842d78f90d074fe7c1c5c2653628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eb535caac06d2fd1661d43b97e4db5fe692d24b125d8628bfa5fbacfa8efe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ae581bd58afa70e8d8a4774cd3842c68342abc749c7bd00bdac51de0e399ace`  
		Last Modified: Tue, 03 Jun 2025 21:39:10 GMT  
		Size: 7.3 MB (7322833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f5bd6045ba459831503398ec4be1e572ad5323c38d12bb6730e8adfacbe98f`  
		Last Modified: Tue, 03 Jun 2025 21:39:11 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:347c188774acea7cac0f2f75fe8ecaa634418b792ac28b30cf2df66f9ab357bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273080946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caadc596f5ea26b8189767392bdd21c06d934530dd8b4e56bffe0abffa8935f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23085f00cc2fab5db834062a7c0906b2e2764d3635d1f0a0795de617ce89767`  
		Last Modified: Tue, 03 Jun 2025 08:54:41 GMT  
		Size: 138.5 MB (138492460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609640a3b5f4eb42252b4f8da7c75f750045321461e7dfebe04bb47459c65ad0`  
		Last Modified: Tue, 03 Jun 2025 18:38:33 GMT  
		Size: 86.9 MB (86856034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb57208bc5f371ce0be7df48e2f1b2d0734b1ebdf45949f2918c41b81f451f7`  
		Last Modified: Tue, 03 Jun 2025 18:38:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14556201c47a89cd2882acdcdbe484ee8f8d32c94a390344116752885dc420f8`  
		Last Modified: Tue, 03 Jun 2025 18:38:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c9866e593ea32e2776c8395eed9bda166a1ee00b92cb766e8d13014e1689b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea8170acd48e15f07532838ebd78cbb81240e8d77cb4fd6772c153667214946`

```dockerfile
```

-	Layers:
	-	`sha256:d134c7a67259e70357c660abd6cabd736418a5536267f972fd459bcff8a9d19e`  
		Last Modified: Tue, 03 Jun 2025 21:39:17 GMT  
		Size: 7.3 MB (7304408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940a6e461a25762dc83c8a9994c9244aa69dce4d23068f037ed9a900e6b3d024`  
		Last Modified: Tue, 03 Jun 2025 21:39:18 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f7ebc5b5b59390d70ae9c94751cb6f0f9c8f413fe8bf710e2c8436ab895c734c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272949954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acec9057fe8ee8ccdd382ce246b5efa4c60d9736b315e44283a612e22d388c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3774d10487b032eb1a2167ed2afb6c687158159ce2ed561584cd53595528c`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0c596d41d21a947efff471afa38ec61d8cf66e6ec6a07b5ebf1846aca66af`  
		Last Modified: Tue, 03 Jun 2025 18:35:47 GMT  
		Size: 89.0 MB (88953138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b3fd3840fd8f53345fe08b5ebae1c9e94e1dcfb31d06acfa5a1a195745affa`  
		Last Modified: Tue, 03 Jun 2025 18:35:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cddea6c461131a4a332c5ab8eed664b9566f24136fe17ea54290c7ae789cce`  
		Last Modified: Tue, 03 Jun 2025 18:35:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e156f72741d2b05edb12becda552c623f5de55249580f6e4f39aece85a65e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7330135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf26d96e3067f640762d4b9fd1d929e4443ac7ebb7d490cae6509d4f80edd4`

```dockerfile
```

-	Layers:
	-	`sha256:4cc1621b615bfda5956e23d69915f8328a7c440b5ceb8aa89d7131e5fbede2fb`  
		Last Modified: Tue, 03 Jun 2025 21:39:23 GMT  
		Size: 7.3 MB (7314338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c90823a04b46d0520a33154acbc5d533741a96397cf8f1f7d068ea5459525c`  
		Last Modified: Tue, 03 Jun 2025 21:39:24 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
