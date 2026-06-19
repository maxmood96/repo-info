## `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:fcf4ffa3a394a3fd31c9b91aeafd780ceb6905db5a1f76ba7bb0d9a2fbd4ea04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2e641011b298c8bb7684919b1f68b36586b9e5ec82ae7b0b72635dd80df82bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175483955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb04ae8772ba3c5caae52892a66b25515f9122cda354dc0ddce8f098386d08`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:11:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:11:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:11:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:11:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:11:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:11:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:11:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:11:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc932f99d75057ce04b3b7cceee4284bfa57bd3cabef1a3ea73896806603b00`  
		Last Modified: Fri, 19 Jun 2026 02:12:09 GMT  
		Size: 55.2 MB (55198721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d4f39d93fe851159d8cc0e32ab49478d11f8bf9acd1fe6c31b83e241d6f204`  
		Last Modified: Fri, 19 Jun 2026 02:12:09 GMT  
		Size: 66.5 MB (66512822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08141ccc28d1cb01a753b9467a4b40fd5669c3d9c43fd8273b67394341b2948e`  
		Last Modified: Fri, 19 Jun 2026 02:12:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23e3edadd332b505b263612cae83794af76d11ddb59e28f1455d8b9cd0f6b954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7541781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54cd5466160e56749a9e312bfeb01c3928796c902e49e6c735ccbfe84578922`

```dockerfile
```

-	Layers:
	-	`sha256:2d432d7c9f564d9d6abbab4be36fe7fc82919ebdf27c8d46da340c2e8b97e2f6`  
		Last Modified: Fri, 19 Jun 2026 02:12:06 GMT  
		Size: 7.5 MB (7527433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8cbb91d2f3cc0769a38e94b38bd4b5affab4e1fbcab9b32c8d2f2c5b640a3c`  
		Last Modified: Fri, 19 Jun 2026 02:12:06 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e49098b732b6390b7ec34387ccec88ec2b938614d22d64a22e9f598273024cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173215235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bfc15bf8ff773a10feef662cc479efcae349f1a65b387fc86c13a5b5e3fed7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:05 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72df15789174e7e6c08669d0069201ff921f04c78f29d2159b41638aa19b0d6`  
		Last Modified: Fri, 19 Jun 2026 02:15:37 GMT  
		Size: 54.3 MB (54272921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ffaaf91043af2733aa6cc0b05fdf5f70513147a1fb92cf465f6bad73ea3e6e`  
		Last Modified: Fri, 19 Jun 2026 02:15:38 GMT  
		Size: 66.7 MB (66677554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814dfc195df396227c3c2d422a594fe1241924615f95bf64467eeb72b1bf7f61`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:766b979e112d7ec0686c986b6e667b7d25cee368454c2b7c1ee16fd9dcdba68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7547698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816fb60d1c64e1cf31a028a8dfac2ade5d09f162e13602ab145612162363f87f`

```dockerfile
```

-	Layers:
	-	`sha256:940cdd695e0c494ed017a7e064b4bbc95736a79613a49bbbb5b0b5e2f42d7748`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 7.5 MB (7533232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb7afac99998b6c7c660e7eaeb6589f01b7af0a68fec044d14c8a385e4eaca7`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
