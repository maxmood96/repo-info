## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:a0bf0fc523a2433126e0564b300d8728ba2eee3c450b833e21aa0761b75d094f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2b257a2dea99e99f1eb3e50d3bdd3dbb4982e25c8719c5b98965f5b9159deff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156501513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd912743d2a294e7ddc641757216f811dc0f0323d59e8da952b69634ce417051`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:22:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:22:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:22:23 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:22:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:22:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:22:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7cca6853d2cca9ff41ce61d72c00c56ec48ccc1ac83dff47ba015bc7903a4`  
		Last Modified: Tue, 13 Jan 2026 03:23:08 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e327184e6220c19d0bf8296344f4743426aede05a3e95e70bd420d200f4d30`  
		Last Modified: Tue, 13 Jan 2026 03:23:14 GMT  
		Size: 72.0 MB (71993820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8d457a4374440565ffca3eeaf99809cbbf0588211d2f6ab24b27cf74894d3`  
		Last Modified: Tue, 13 Jan 2026 03:23:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d50f2303e27a113aec70d9048c6313d72173e2ab107c401f8aaa16aeee52b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f05689a8b679ce152154e65239254fc4440f422cc6c0fcbfc9c5c9bc69ff7a`

```dockerfile
```

-	Layers:
	-	`sha256:a08ad783361090c8b855e979135cb60c4e6299ee5b8a1894bda287c254f8a594`  
		Last Modified: Tue, 13 Jan 2026 07:49:37 GMT  
		Size: 5.4 MB (5377905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67e980b3f94a7bcf38818f6c895776faf6239b7e826c8bf74b3fa557ad7749`  
		Last Modified: Tue, 13 Jan 2026 07:49:38 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd282a52b515808881943aff6c2c8464c6d74634239da9e54e5fc74b61749b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155755861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26a16a65d5ac72a4e0370a11fee2b493b19cf3d759536133550df2199e26f6b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:28:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:28:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:28:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:28:15 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:29:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:29:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5480ba41e3bcfb93e424f39a4c17f892847d2e9ebd790a09ce51b8ec2ece28`  
		Last Modified: Tue, 13 Jan 2026 03:28:57 GMT  
		Size: 53.8 MB (53814999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de793f8c3fad46806fa5654e7581275dd4129284e31a4ee3b74792bcfdc4b8a`  
		Last Modified: Tue, 13 Jan 2026 03:30:13 GMT  
		Size: 71.8 MB (71806177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54aa9cf6c672b2aa797757c089ebe51b8315f8a4b2ad579ae85470fac838c4`  
		Last Modified: Tue, 13 Jan 2026 03:30:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae76bff555fdb664dfc29ad69b85a98e106419d6dbff11d91f4d9154bd0fa01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3962ea959e8344dae0968c34f7db662d30eb4b2e13d96cc538d85455c1322a6b`

```dockerfile
```

-	Layers:
	-	`sha256:6dacd5e627aa2f4592e6b6df241cdac8a1da78ecace23aea85c493fad4b0090a`  
		Last Modified: Tue, 13 Jan 2026 07:49:43 GMT  
		Size: 5.4 MB (5384372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb1c46950901259849980c39d83873cbfb731f899b722fbda5f31bf4f6577b4`  
		Last Modified: Tue, 13 Jan 2026 07:49:44 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9fff111fab73f6287e8ed6598c032cfaa4310fb4d76a413bcc0fa5a3f48f8945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163161341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5d63b7f000f95acad74f5bf592ac30eadec2ee8c171d083c6f76f43a8c825b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:33:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:33:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:33:27 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:36:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:36:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:36:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb058f93a6c678219fa0885fbd007fdf97f1d78e5fc8118492f88df378530b`  
		Last Modified: Tue, 13 Jan 2026 05:35:01 GMT  
		Size: 52.2 MB (52175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4bb684478a25ea733813c3a0a926e0026c82ee05d77dcb947320e0435308b0`  
		Last Modified: Tue, 13 Jan 2026 05:37:35 GMT  
		Size: 77.4 MB (77389936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe1ec931d87e792be30ea4cbfe3c70902d741e02bef9df3dde838c87c31ce9a`  
		Last Modified: Tue, 13 Jan 2026 05:37:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b14377761b79c668bdea373b623497d956b2fcdf434ca6acce5d0f35e3f2ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26bd9f25dce3a196322cc80467448b983da97caa156ee3b3fc5816a033341f`

```dockerfile
```

-	Layers:
	-	`sha256:b2a551799689c0af0cae67f26c35ca3eea420cc634b07a141c0acd1efe301878`  
		Last Modified: Tue, 13 Jan 2026 07:49:49 GMT  
		Size: 5.4 MB (5382869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d92bfd6e4d9e69a5b5503006264c42cbc6858e6429fc6223d0eee5535d3b0d`  
		Last Modified: Tue, 13 Jan 2026 07:49:50 GMT  
		Size: 13.5 KB (13476 bytes)  
		MIME: application/vnd.in-toto+json
