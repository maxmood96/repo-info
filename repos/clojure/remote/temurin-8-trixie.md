## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:db3b805c5b5c5c445aae8e5047ffc76bceb1e07b61a37c52a3a535ca80d2c2b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5ce87592298205c13b05862bf821eff8bf506a5ab089f619968a85b07bb526ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192186527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa04b8229b7097e70c9a37349fe981f6b3aefce429bd2400a5daa86aba8aaffd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ba0099e31d5876895014c5273307078ddd690c1f52f2f98d8b9b4dec0e74e`  
		Last Modified: Tue, 03 Jun 2025 05:15:32 GMT  
		Size: 54.7 MB (54716190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800ca6161cb73a5cff81ebab1234450a3d7b41340aadf88e80a736aa084706f`  
		Last Modified: Tue, 03 Jun 2025 05:15:35 GMT  
		Size: 88.2 MB (88222785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0200f6663565b580ac2a7f173d82323696aaed2c83153d11459d445122db63e`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f9fc0158dbcba87d987ba09e8f837a21d67c764dd27b4b28c922e9d3fda70c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7454238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c04cf7d5e26c78fbb046c6f31b0264d916a0f9c54625ebd5cdb550452d3c73`

```dockerfile
```

-	Layers:
	-	`sha256:36d1c26e7bb69adf16677a6f5a13423928ec1d878bee7765cc1e246e83c08df6`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 7.4 MB (7440026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1099f2508c6fffa74f1817db0d86c54e1504a8f9ae7e86c53294c2b860567c3`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e66a6a4bae23d65999fd0ab15666b5acde0e020488f76f845fe4b9748b78e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191955338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dbd6c0d1cefceb5aa6defe370a89fe8a881d8e07bf8fa41284fb1718bb01dd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b438f9c0792eeeaa8637b24f8c401b4a12e19eef04c099112c78a727c9bf9`  
		Last Modified: Tue, 03 Jun 2025 10:32:24 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c62ac4cad6e3627b6d4f3e599965aad7622e778e4876ca906516cbb06ce782`  
		Last Modified: Tue, 03 Jun 2025 10:38:25 GMT  
		Size: 88.5 MB (88505883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ebdf3025482ea139e9cd7ddd9e9e5a68bfeae760d7d27705ca12e49ffcc9c5`  
		Last Modified: Tue, 03 Jun 2025 10:38:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:21108f969732a77138d72b9eafa2b0762a39e1bc981e585e3cc47f0005b3f5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa935b3dbf2deafbdbd366c8ed1fd58cb84a4ab0da183d518e463de1b586003`

```dockerfile
```

-	Layers:
	-	`sha256:bf4d2a2ce819db4d47524c4b9a9b7c9f5d349f46310d2d644b0efe1008d95eb8`  
		Last Modified: Tue, 03 Jun 2025 10:38:23 GMT  
		Size: 7.4 MB (7447754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d993579ec68048ec2018742548375aaf3c801da8730756234e56e379eee41902`  
		Last Modified: Tue, 03 Jun 2025 10:38:22 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:302450fd9be2631df97916af897fcd634e7034ee1e01f48536dbcdb2361abb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199205665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966b576d3d417df6b87286f86ec6e24f2615fa9b81ed1060bd6ad6e22101869b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975f5c873cd794ffce77448d785fd1ca79428164a5e8dde7131d18ee75ac676`  
		Last Modified: Tue, 03 Jun 2025 08:10:49 GMT  
		Size: 52.2 MB (52167951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acae88b27c993ca0256c028af97df5f5a4ef95343f6610534278e1268ecbc88d`  
		Last Modified: Tue, 03 Jun 2025 08:21:21 GMT  
		Size: 94.0 MB (93956525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2037ce693f6b033e35bba8ca6aec0bbe1b06a0edce72860eed56908b7eb0aa1d`  
		Last Modified: Tue, 03 Jun 2025 08:21:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7ebfd8a0f567c902d214feda089a529ea5f4bd4408efa505ba5910e00705c357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d8ac7a5203d23865951f26046408090b5506ac33065417ae210f96875569c`

```dockerfile
```

-	Layers:
	-	`sha256:0d69cd1d298ecf0149fd1d221a12b49f0b2e89b0d9f259cdeb8a4836918f7f5d`  
		Last Modified: Tue, 03 Jun 2025 08:21:18 GMT  
		Size: 7.4 MB (7445036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb43cda1f7dda4c9ce36b8076290a42d60c503e072ac69bc8f9454012343b8fd`  
		Last Modified: Tue, 03 Jun 2025 08:21:18 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
