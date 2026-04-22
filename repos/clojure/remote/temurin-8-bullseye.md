## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:c181760d6b91717cf117c0b0cf541af5ab04f869fb6893c36175ab13755caffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c5bc5310d8e4dc7828ee45f2e83006e85ebb7f6c69316d932b606e156bba5d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178531432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf807c19e8309a267374c654e26487a16276c90e8aa3d91aa1e9d108022445a2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:16:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:16:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:16:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21adc4c44075a86a3eb25e62c1f90a537c10b34c8c656d2e2d9ee27f92c33e6f`  
		Last Modified: Wed, 22 Apr 2026 02:16:32 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431e5f0cc2acee11d6cf05637507be63c835919e84777fc89c3948cc6700d97f`  
		Last Modified: Wed, 22 Apr 2026 02:16:33 GMT  
		Size: 69.6 MB (69597578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4dc0e200044f69c4ae36978d956e2b3d7f2cec381d9e9d7b812bd798c16462`  
		Last Modified: Wed, 22 Apr 2026 02:16:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dc99ca08cadc0ffb6b89b8b9628d6aec7956dddfbb75b9e1e8bd96e4e3002834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa8f514ab077dd54840e8ad42261b519639d7989957a32ec3ada446f6c2ac5`

```dockerfile
```

-	Layers:
	-	`sha256:4dd1c16e62341f9d1bd2622268b282b2bf55b689a05d94a3cfb92cd32f3c6946`  
		Last Modified: Wed, 22 Apr 2026 02:16:30 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb74483bedf6c5c7ff5548a00fd61ae3f38f94b410d586ff662bbd81abebac2a`  
		Last Modified: Wed, 22 Apr 2026 02:16:29 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a475e3389b863759c06d0a07a86a8f5d8f49adb869df3568cee56caa2f30bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176243628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc735620b4ffda93b6abb7d967cdca43f56e5319b4988716ccc502c3b3827bf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc9e2daf87d570e7e17e66a484c9dcb113fa3b2faf09639a0d88a17f53177e8`  
		Last Modified: Wed, 22 Apr 2026 02:19:29 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d39dc96142b2e0657eb81d8db03e28bbd77f47e6dd1adcd6094e2ecf2bc966`  
		Last Modified: Wed, 22 Apr 2026 02:20:14 GMT  
		Size: 69.7 MB (69738371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae1167448cad3a0cf0a7a04f3d3b0460b78eff1a46df407790f70017918db2b`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7741eb6b60111c5da276c7cfbaa7aa94bf12404dd1ca28dacc5427bfcdc67c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7547951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3b312f7b02322430c7fdb85340fb2f083e35b7e224c0615dafe5c63231520a`

```dockerfile
```

-	Layers:
	-	`sha256:2e3e1c871f9b1c4301990735d157b9315b7f8bc57783487c78cf7ade3f007ab4`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ec7cae8780778788c570a1e6ce9dc7a4a585e691ab8631dadc9a32d4684310`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 13.5 KB (13512 bytes)  
		MIME: application/vnd.in-toto+json
