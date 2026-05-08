## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9ceb225d45d2840847baecfeb93bad1cd91cbcac4a5f0675cba720d0a82c1854
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e695fb4f8f489c3be4e16640634d8d236a7a34280b488815091e3c59d406c0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235350767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722f2f0f0d33628fbc7effda836b1a2cea154a2ce58c824c87f661f47b06336`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:07:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:07:49 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9349b195aaa39077c89642f42ec93245a4b9dd487707116228031eb4cbf3708`  
		Last Modified: Fri, 08 May 2026 00:08:25 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ed69ab30457fdf624e3f5e94a884ca582887d750d8c1a04c402b77817182`  
		Last Modified: Fri, 08 May 2026 00:08:21 GMT  
		Size: 59.2 MB (59186306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c93feb9aec65c4d73800f29e899620b0c38804606e57676c38c294d147af`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41060b7c2f2f177273ad92afb54c49625980d5c5724cc5befbc4474b9e31bb8f`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36df7f33e35f5061a6b7195628de5ded836aef32eeec52fbe38910d84169ecc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31d2d24d6e01d7ba1af727a08b9b96adaa7809d7961158e55ccce5508fbcc99`

```dockerfile
```

-	Layers:
	-	`sha256:8e492e9df49a4b35101ac88c87369434e8e15e675f6c7396c2cee0d24b21ddc4`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 5.3 MB (5320680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6533157c938d5c381ceea8de7d9474e9b64d4354f5623027a9905ff14c2fde7d`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:604c2ac9d807f248d7c857d921193bce3e7954e967a19069cc0f8bf7dbfc3863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232799055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3816f8e4b28e12672d4b669611995312b46240c6f0694a6c156cb8aed037e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:09:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:09:43 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:09:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:09:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe960c7261a53a6fb4074a3da4f13d4d2fdd424efd0ac5519293d2af49aac4`  
		Last Modified: Fri, 08 May 2026 00:10:18 GMT  
		Size: 144.7 MB (144724353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada707a391e2c123bacea0b3ae9cae1a07482be059fb936b1852d8fdf3add66c`  
		Last Modified: Fri, 08 May 2026 00:10:16 GMT  
		Size: 59.3 MB (59331152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181c11f281b6ba15ba9c99997ac580eddeb8a0f875a1cddb1652615232f2f6f`  
		Last Modified: Fri, 08 May 2026 00:10:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9666c530c739e47139790a21c33005929edfbab40f5df0d3ed802f62240446d5`  
		Last Modified: Fri, 08 May 2026 00:10:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4425d93dbec4ce2a47fafb5d5ab9b87454d653253023568dbf193ed6995af78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ab356788627838ecb6906fa56d5b4a44d4c5e8f5a77fb7e11c5e7a701d1cc1`

```dockerfile
```

-	Layers:
	-	`sha256:15ecbeb93e72e6b48ef348683720e5c8602f09280e1cab420de4af98d6ed33d2`  
		Last Modified: Fri, 08 May 2026 00:10:14 GMT  
		Size: 5.3 MB (5326412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062fadfd38b5a1aeb052a755e0abdd2bb35894dd977fc3b7abedb36bd0b77eae`  
		Last Modified: Fri, 08 May 2026 00:10:14 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
