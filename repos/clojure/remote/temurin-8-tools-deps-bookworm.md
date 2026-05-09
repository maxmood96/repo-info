## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:5d1061f409484e283e1cc64160bd5cf63eae4092eca8ec868e35bdf9c3606c6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:fd2a74ec6d54d9f02ad5cf8c53be374266b1037c2be92a7e1cfa1f98322db8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184826022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7db7c1642e5e42cfeda3dc6598da725d7f9e58bdfe4c8bc0d56b997736f847`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:14:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:14:42 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:14:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:14:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6a842ee2fc9ce0139183c0d9de4ca3dc49f0fa9aa236867cc056a8a57416cf`  
		Last Modified: Fri, 08 May 2026 20:15:17 GMT  
		Size: 55.2 MB (55170047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a5b70cea400fbe90ffec057b28239df5f735f3da8b56505d03e81cb71e4188`  
		Last Modified: Fri, 08 May 2026 20:15:18 GMT  
		Size: 81.2 MB (81166653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd815ff9e716a4c9c4e96dba97c4dbb8c1c65c8dc392d01676df6d592fda8b0`  
		Last Modified: Fri, 08 May 2026 20:15:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a403709d90460773a9db2d697eea7f28a84d754a7499e2f7438ecb30fc0df9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9837b784c081068e04ebf6c07de10c91b780a12d98903b55f5ee48e07648240`

```dockerfile
```

-	Layers:
	-	`sha256:e2aae6cf5678f6ea6387fd4ad83f6173b38aac2ddf884db317050d7aa8702136`  
		Last Modified: Fri, 08 May 2026 20:15:15 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed634983a196853d35945ab5b0195f228786537583e3ead44684c3276ef01af`  
		Last Modified: Fri, 08 May 2026 20:15:14 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:125ca8349e916b6d50e71b1bf418e9bb8d102e430cf3ea5fda60983d4afbab08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183799505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c073087db7474d8134e6e35af2e7b98161b6ff179d7b542b8f97f69474c23d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e641cfa1365baf959e0831e12b0ec7c5ef82d8fc9983c72b3b3e700ed206e89`  
		Last Modified: Fri, 08 May 2026 20:19:21 GMT  
		Size: 54.3 MB (54251618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee4fc77f8587a63ac72977406239ea37d2619153ba85d3a1c18b8765605d191`  
		Last Modified: Fri, 08 May 2026 20:19:22 GMT  
		Size: 81.2 MB (81174091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a4409373912fc0851e2025d4bf0fc51efdf0c98b8d03b859661fd10b91ba3b`  
		Last Modified: Fri, 08 May 2026 20:19:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c7f3ad85139f7e0c16470e67e486d4d882b9c8a83955fa4df818f71994ccc087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40e919fce7add4f244f7b6f7598fbd43cfedaaa31af922a8e092d32fbe6863`

```dockerfile
```

-	Layers:
	-	`sha256:380fa9e5989a70187f1b017b5e1f3040aa287700263c1805a7431f7cce4b9dc2`  
		Last Modified: Fri, 08 May 2026 20:19:20 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae63e1532725b06f09d390c54ba96a271cd495ca9094eac937cb90d0ea1a3a1e`  
		Last Modified: Fri, 08 May 2026 20:19:19 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc9ea52e92405425f7ccaccc00dabc94a2b223145d6626791d435106ed47d016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191991379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0ddab4b7c001c613e437f8f437ccce714d6a073bcb4757614131eeb79bd531`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:13:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:13:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:13:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:13:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:17:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:17:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:17:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d0ad1b604097f835cf3ae8697f2202d5324bd2127f91a122d7bb0676b31fcc`  
		Last Modified: Wed, 22 Apr 2026 08:14:28 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ca9331a673eddf27bd2cabbbd032b848fa650700485ba44760f7601f16602a`  
		Last Modified: Wed, 22 Apr 2026 08:18:34 GMT  
		Size: 87.0 MB (87003611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fadbb8ba324aaa4d30c388dfac74758c7d42935093379a21dc7495c9495fe9`  
		Last Modified: Wed, 22 Apr 2026 08:18:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fda403dcb2df0fa0a8bcaea9e8baf5013128e51c6e7eea8a246666af6bee8b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2484853029f0f92b35f27799510101e98610131f4b1bb76d05246742dcdfec0a`

```dockerfile
```

-	Layers:
	-	`sha256:e3b75aa2005f1439f864d5f23db5443b379d5d00a37ad548fa48379f86ffe6e7`  
		Last Modified: Wed, 22 Apr 2026 08:18:32 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc7461272ad5c0221e2bfddb4a0d5c7b10a0c022d4be8ae592dc692231da095`  
		Last Modified: Wed, 22 Apr 2026 08:18:31 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
