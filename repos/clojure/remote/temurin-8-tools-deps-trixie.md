## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:c8fdcbd8e3f09143f3df30ec549a4a0155c3a3e6da45eb23ab97e27c308232f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2918668377c2b32c881d8474eeff5c52e71602911ddb0981079de9aa76573f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190035826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20982285013e140404f892ecffb39eed36d484b8eed1db3a223b1deab7b45a0d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:56:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:56:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb05b96138d4121430843048ca214a7dd2bdc6e926c029de49395aca2fbfdb`  
		Last Modified: Tue, 17 Mar 2026 02:57:04 GMT  
		Size: 55.2 MB (55170145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba28537a803cedb54a6a495b4949ef78f4e27bf9602de30823f6df7409f90a66`  
		Last Modified: Tue, 17 Mar 2026 02:57:04 GMT  
		Size: 85.6 MB (85567507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8049f6622b12805adcbff68b0917a7693868e5bced77aa7028ade41b599294bc`  
		Last Modified: Tue, 17 Mar 2026 02:57:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:715d2cdb513a19cc151bc6ab926a812371c942f9b314c6b38ba93e9061da65bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30417cddaa456f5e474175afba68908fdbc365f6f69e4432c42a3ceefbf42f96`

```dockerfile
```

-	Layers:
	-	`sha256:42282d8f68c47331b34e270c0aeaeea2cf13915d27b8b0bd9919f6d5409db96f`  
		Last Modified: Tue, 17 Mar 2026 02:57:02 GMT  
		Size: 7.6 MB (7591654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a69a27748ac4251a47befb67ec873cc94787d29a26ad87964e52fe876daa59d`  
		Last Modified: Tue, 17 Mar 2026 02:57:01 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8faad4c5737e79a33e652799f6c46ce0f35ec4196b4964233bd87139dccd813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189300160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb61d0a7cb180a791930aa7e979461527c7a66d93bde802462bb535fe7b76981`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:19:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:19:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:19:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:19:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:19:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:19:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:19:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:19:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0f8c28e324786fc49e29c5f13c3a3fa558dce1fd093786571ec6ca46aad6d3`  
		Last Modified: Tue, 17 Mar 2026 03:20:18 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24143bbce730fce365dab16c01f3cc228a2977e2e74db2af93ab0725d78eaf3e`  
		Last Modified: Tue, 17 Mar 2026 03:20:19 GMT  
		Size: 85.4 MB (85382953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af744ec8e4b03dbf7e18dac82f7866f9dd960b1c231245958cb8923ba6dc6a`  
		Last Modified: Tue, 17 Mar 2026 03:20:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:48c2479ce0400d4246f4b33db67a35be66b2a8aad38e7b59e1a8f95601dd5239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9198c31e95e05fe7e679676dda9595ec77f2de9803752ddc32d7ed01bf0ffc23`

```dockerfile
```

-	Layers:
	-	`sha256:15b959f033c702d1e728a2301bdf2e302bf227428da6debde6e26154098690bc`  
		Last Modified: Tue, 17 Mar 2026 03:20:16 GMT  
		Size: 7.6 MB (7599384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d66f63e410272b6353c403c93935afaa94798d1ffd410bf749687d495829a89a`  
		Last Modified: Tue, 17 Mar 2026 03:20:16 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ee255fd6253c71637039b85f1fb6e17b1672ade342c3fae7b053750df5fdfda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196739968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff40d5a04f130f6575ae16f2802af4841520b3b030e9d8b0e9f28945221961e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:43:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:43:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:43:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:43:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:43:50 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:44:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:44:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:44:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f433cd6a7592bc48b33b544e10a803a205a566330f6a483acd14d8b1279a0`  
		Last Modified: Mon, 09 Mar 2026 20:45:16 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3309b696921326cbaa9badf9d61f8a1348976a407d6a70c8add36ccbfcaebd`  
		Last Modified: Mon, 09 Mar 2026 20:45:17 GMT  
		Size: 91.0 MB (90976671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a1f9e43b8c502b18d7896b52282ea15e0d6c063e84cec2f05faa0453a21fe`  
		Last Modified: Mon, 09 Mar 2026 20:45:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3d0bbfc6350815ac6425f715ec7c5e44f87b18c5b0b1e02b423208dbdff220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff9ba86e88ff826aa6a7158ddac32f0a52924dbbf5cd6e6949063e4beab6ef6`

```dockerfile
```

-	Layers:
	-	`sha256:6f786c2068fe00da6a2c04941d71a58d7ae6748ec2301245f99cec89a874307d`  
		Last Modified: Mon, 09 Mar 2026 20:45:14 GMT  
		Size: 7.6 MB (7596596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942895eead4b677a45ce173ffae3a8b927b936267e10e9583db25d40f8e9dc16`  
		Last Modified: Mon, 09 Mar 2026 20:45:13 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
