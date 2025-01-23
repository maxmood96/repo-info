## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:6d8ab7623763b1a917bc8233a2d82187fe093a2ae30f3d93f3618cce97e388ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:acc3fda51246d463c4a34e5e041b92ec0500ae0713a15df4ec859cd9f23011d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bb64632e1d77e11bfce9fbf3510e753a144d1a80c5129a976ce650f7bdd9e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa3d69ccb77ff6de2f635c97308a8572aed742c141aca82562820a87d64bcb`  
		Last Modified: Wed, 22 Jan 2025 19:42:37 GMT  
		Size: 165.3 MB (165295135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbd4113f2eca4c739b381186e78924aa42a7f9007dbd729c53d80ed3c6d53b8`  
		Last Modified: Wed, 22 Jan 2025 19:42:36 GMT  
		Size: 69.2 MB (69178471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84be987bbb30377aedc29d3ac6fd5bd835ad1b3c0f1415993dd96894cb131c9`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f661ab0a5fdc01cadab02ffc40660b91196f35fbf3b04b2c3cf944eb6c602`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7eed94775198dc7ad20c903dbda6de21579e62ea114082ae1fbd5db2440b5cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989943abc6bc3677af3233a6cca37029ede17876b5befc8e1a7cc753e0d2b932`

```dockerfile
```

-	Layers:
	-	`sha256:1bfc9813dd6b2af143a871228fdbf4f9fef905a5d53aee6df3710d74ac395e4f`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 7.2 MB (7209562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a600bc465a562703ba8efec181ada78b3cb1d288797a31448b64134f254dc1f`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:abdebe231fb331254f01bb3242859f5304fe6b5c23f925afe0bc112bbda41fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284833271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9207588b50f6e2400cf092fb388a69f3acdea4965c074cf9424cb9e1dd9cb4e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c88310eb31ad4db4b3db751bd323c682dbb85882175deb72e3eedfc84723`  
		Last Modified: Tue, 14 Jan 2025 12:40:53 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019d59ba34535ae3797f33f955e8303e6bb8756e439dfdae64f4b72698ff663c`  
		Last Modified: Tue, 14 Jan 2025 12:44:07 GMT  
		Size: 69.3 MB (69304377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc50eb82da6a4fd182935767dc6a8eff26a28f49fdee9526f834500ef427cdc6`  
		Last Modified: Tue, 14 Jan 2025 12:44:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc218fcb751e994741ba3beb4d18d1fcc475c83cb43a3280e4c96ed497bb8a`  
		Last Modified: Tue, 14 Jan 2025 12:44:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9919fd2ef91f1a7e7377bb1b046ba865a38a91628faa905e031445d996e3444a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e89fafa4e6fa3823cebbd855a509c0b2b022b8c9045a911779fe95f4719bcd4`

```dockerfile
```

-	Layers:
	-	`sha256:acb19df9438992e749e81fd0c0c7eda3f414623328dfcab9a1948368f1216bff`  
		Last Modified: Tue, 14 Jan 2025 12:44:03 GMT  
		Size: 7.2 MB (7214040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832e736877ee98d2b9b1cde8334549ae2b3d3b3bfb871cf1219ddf945da1a15e`  
		Last Modified: Tue, 14 Jan 2025 12:44:03 GMT  
		Size: 15.1 KB (15138 bytes)  
		MIME: application/vnd.in-toto+json
