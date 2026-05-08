## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:86bc9c8975762e32cfee80df6b4a205e138793faebd3e9a5cce0f6fd29389fa9
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dde1fe88a190b1a8cd6eab3f1ccc052798786058db159ab606ca5419852a0350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287822902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f7ea7d7595b042955a575c337bca1e120363dc557dcd1f38850c76bd698987`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:27:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74c3bca3282b3d3132e1c20a91a9957f123499e0489e3e5e8dddf70f973691e`  
		Last Modified: Fri, 08 May 2026 00:27:48 GMT  
		Size: 158.2 MB (158166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acfa47e0a56628464402de1f61aaee1f91af1e7b501ccc77cecdacdbc5eb05e`  
		Last Modified: Fri, 08 May 2026 00:27:47 GMT  
		Size: 81.2 MB (81166297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a521f9e74964610a74ddff5a031c8f565fb2cfaf73b23b72ee897d26fcfd0f70`  
		Last Modified: Fri, 08 May 2026 00:27:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cffbff5227bf86b05357b4f511ade88bbadb7be32cf503a1f073715da9aecc`  
		Last Modified: Fri, 08 May 2026 00:27:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f9c3380a156915769f099feeeeb61c1a50e1077d645c48fe75b432be71e781ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1f1580b0625bd5a330b79fd93da4c322221cf2ad8adf59f7e72421977986cd`

```dockerfile
```

-	Layers:
	-	`sha256:ee4ae477fcbac60f4754fe83273793baeaca9c560b179330a1684e40dfc07426`  
		Last Modified: Fri, 08 May 2026 00:27:44 GMT  
		Size: 7.4 MB (7381465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63a4cc2c6815dc792ba165cc2985e188fe32869e1e5aa6c6c12d7ee3f674186`  
		Last Modified: Fri, 08 May 2026 00:27:43 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48afeba190e141f638bb70cb2f483377051bd8840858b99cd66c6cf8d241550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286009435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777297f834e608b34fe43fc4eb3f485be470dcf1e00b29919debe45f2bac6bc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a14438b793e27c7006f5f44a3ae858cd4a17fd25d3dc6d60e2305e2a40fa93`  
		Last Modified: Fri, 08 May 2026 00:26:55 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908331de17f4004f0f57da24523131bbde1b195fe327576c07d46336f63e2f0a`  
		Last Modified: Fri, 08 May 2026 00:26:53 GMT  
		Size: 81.2 MB (81174077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d9e7f67666aaf8b0a64a05ca1631ce89810d6876cc10619948a8c990da2d28`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ffff3d7b0f2297f9bc1c8f2dfd900b4a0b16d3a3bb90e24b2632fb5b79f46f`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:84cb2ff8a850fc0162bab41b83f17d9f759981bc90922e7c14ddcef54413fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beefd63dfa62866c228282b7ee4124f923be2c745e2a6539a6a06a9bf8886005`

```dockerfile
```

-	Layers:
	-	`sha256:a8dcf5811c913247fb49aeca8a18bd540dd07ed902aeb40ec23fe0a63cc6942a`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 7.4 MB (7387252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfefad745d4ba85f83212dc4fc8fd98f1d807b572311a72d6e7a3beec3e7f3c`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d1c66697ec608f07ea28dcced3045b4e24468a5feba842de0ab2546b20dd58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297685170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f542482474e69fbd70c6af86a045b26cefce486e81d67d0b62423a405da85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:40:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:40:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8e0b4789351557860694b46272535c93117f7a4691328b094ce2686e9cf5a4`  
		Last Modified: Fri, 08 May 2026 01:40:43 GMT  
		Size: 87.0 MB (87004156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaba1804922b140c687efd6ac4549912e9bd9bc330683f54b12c24909bb597d`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0ecef2f15021651346f5987602abf46f737c2ec4425f7706698f9b793427e`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:227679f74ffb57a162228e77838bb7c4b11215233033c07053046c5c2f9ca280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651970740fc77dfc0ac1c0090a9d4f5d185e143094a1444327c233b0d4e00902`

```dockerfile
```

-	Layers:
	-	`sha256:d0c209e45ae75c7b9991561c4472184b0cd6a9fd0946437638689394730fd0a1`  
		Last Modified: Fri, 08 May 2026 01:40:41 GMT  
		Size: 7.4 MB (7386693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e361a8246910435e103755fa5cbf2158ee2c284078498cbef639e138d42b3a20`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9951ead258f40b6bf177b99175fc5390603241d7e2f26759fc2d3e9590c9b5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274517146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3694ee627e221fe8ba4695ff6fa210cf4db831d269a7159182d5ef3db0debe5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:38:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:38:17 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:38:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:38:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:38:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:38:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:38:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d702ada2d7e9d00abe722366b56fc0be0dcfc2ec7236668048bc2c5e0273e1d3`  
		Last Modified: Fri, 08 May 2026 00:39:07 GMT  
		Size: 147.4 MB (147388367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff43c41bfce0e90f70923e6458f2e87aa101a0592b006f0b1541ba1af60c6d10`  
		Last Modified: Fri, 08 May 2026 00:39:06 GMT  
		Size: 80.0 MB (79979768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6fa1705dce88e2525f6e33e3d758251d97c4f167c5aebbc792cda446845f81`  
		Last Modified: Fri, 08 May 2026 00:39:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38412c08db20aa79f2d5519e5cc8160a2ed1ca7d4bbc4ab4f3f3b0b08bf327cb`  
		Last Modified: Fri, 08 May 2026 00:39:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:87c6b02ffebe00ca57387523970337c69e46430cc380644a8115c5ac80aa4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afee0d0387e29996758c70fe1da8a0e5b4920d1c37afb82f8bb14a816eadde51`

```dockerfile
```

-	Layers:
	-	`sha256:4057df6f50e5c49bbeeba715d317b7fa7416769c33056350e4de2325aef56f79`  
		Last Modified: Fri, 08 May 2026 00:39:04 GMT  
		Size: 7.4 MB (7372784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db42e89b06d79e55bf86af6bb7765a8669acb512c74fc60cfc5204bd1666122d`  
		Last Modified: Fri, 08 May 2026 00:39:04 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
