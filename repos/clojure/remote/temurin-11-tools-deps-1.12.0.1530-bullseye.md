## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:b090c54e143aee24572a7c6fe62b125b49fecd6f52f025b5f715e39d6e42836b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fcbabf0c20f5b0d238e80798c90dae10194b57e408d674fb92f2340832eb5653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268780534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0d7d8f9f5ed0649d0340f28af2d85d473ddf64152f2d1ebd1df2b81f7f46fa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fd8ae85a2e253a4d448bf266b233c771a948c073c1b06e49cc201326e16286`  
		Last Modified: Sat, 17 May 2025 15:42:58 GMT  
		Size: 145.6 MB (145635734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bfa5f1c8554371a2728f42f8ea6b0a781e158f21a2d68e6c1ff548134fae50`  
		Last Modified: Sat, 17 May 2025 15:43:03 GMT  
		Size: 69.4 MB (69396417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923c8ee0bc818424da8897429c7de814ec00303a8649c4b88b3996908c4250c`  
		Last Modified: Sat, 17 May 2025 15:43:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:450cf9d4fc902ec1e3e7424babcd8d411841b82c47656f8c7be66fc34f278162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807e4b176fafa16dec6413bdf54e519ea3cde147822a94673bbec0c5e6581c5d`

```dockerfile
```

-	Layers:
	-	`sha256:41dd9c0c29b25acdd4417b1f1b97de944cdc5ce28844dd61d57cade0f2419af7`  
		Last Modified: Mon, 05 May 2025 17:07:17 GMT  
		Size: 7.2 MB (7226696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c3bcc7f2d1f4bd342dd963bc319377ecac9e07d57123acaf5e3e1baf75b2d9`  
		Last Modified: Mon, 05 May 2025 17:07:16 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94efb1b6ce173c570d64426fc5f389f4cc79a2c754f5356888256af9256af0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264196412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8f3bb03a49bc4a9dbb2dd96ecbfdc43ee46e2017317825b6dadce2230ce18a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d401d739612ca72cd16913778c2bd866095cacc150ddab122a79a1fc7cbacc5`  
		Last Modified: Tue, 06 May 2025 00:25:06 GMT  
		Size: 142.4 MB (142420730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303466606faeeb976ba5df0e6ca05cccb8544aeb66de1d40041d816ab2461e8a`  
		Last Modified: Tue, 06 May 2025 00:29:30 GMT  
		Size: 69.5 MB (69529057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67d06a3e2d8d402d05d36c6adef3cf4d8f5753f7c43fc5eb113aeb231b6c00c`  
		Last Modified: Tue, 06 May 2025 00:29:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a732ddcaf3ac362dfb84ad503269bc493176b7b393f1b74335e6661ab48f8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328e3f5d8fd9c47609036526e8278648acd2b276801c6feeb089c95293b59f94`

```dockerfile
```

-	Layers:
	-	`sha256:5c68dca8a0a8a62a588f3288f365675452608934d04ea13dd95fed38c5b83cc0`  
		Last Modified: Tue, 06 May 2025 00:29:28 GMT  
		Size: 7.2 MB (7232413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1501ef82543266a506583a78f3e6a50fa4aae0baeb0bf6ccf57fa4e4c194897`  
		Last Modified: Tue, 06 May 2025 00:29:27 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
