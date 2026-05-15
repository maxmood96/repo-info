## `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:7ebe3119a146934e7a96df68f121b6b56fd1bcba694e87ac5ee2ba3bb5e13d64
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

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ef9db9b8846dabc01fdf644fe02f9c850ea3853b3fe429904af0fff28a18d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243852949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf66235e7bdc23c63097b9d7b7610e391b802bff433c994d5881c66dd57765`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bd86d57d68e664d67c2da1849fff4d38ea9c202d9e9a24e230e4b07dbb38e5`  
		Last Modified: Fri, 15 May 2026 20:14:27 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3872b5c4f0b615d1131fb47685e136c06a4765eb7965416ba2d7de54f17bcb`  
		Last Modified: Fri, 15 May 2026 20:14:25 GMT  
		Size: 69.7 MB (69729757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a330102c64adbeca1169fd58c9c6c68c4f94e5e5a2b21e1391b7584315011a`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30d4228251ee9d2bd98a3466aaa1232f7b69d23b212037aa115ec72631f0bfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be75048df1a7ad10648141d58e747351e6289fdf0eaec67640628e6635c4e2c`

```dockerfile
```

-	Layers:
	-	`sha256:27a4ef9855c8ca6d552f2b3b387ebecf271f039e4f5fb611d6d622fb5849a107`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7b64d02920bf02b41839231afe7a1e0b35dfcdb06e1777904ff4fdf39f12a3`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31b4e0bfd7ad1bb038d8d98485e2adcb08e37a189d03e26ba18d0eb7a7d1f9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240421785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf23e6d43cb58635e0d332c237301cdb54ad70957edf4754d1344c605397d53`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:13:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0eaba1402f0490b5ec8e81803fdd1cbfd8fa117db4b17650280142d8a84ab8`  
		Last Modified: Fri, 15 May 2026 20:14:17 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65418eb8e37786e7311177c431ec5e0120d6f204af9a755edc5339f12688c4d3`  
		Last Modified: Fri, 15 May 2026 20:14:16 GMT  
		Size: 69.7 MB (69722746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0397a28e499f9e23f6615f922997f07f9ca1d494c99a9167675960884d41ea02`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9652dbbea1c8582c9eb283f9ac5cc5c4b631705bd8782b63ec53fae94b7b92f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96180c5ef40311439a4d6b4062f7eb475d676d1460951379b03b10f6f7c68d0`

```dockerfile
```

-	Layers:
	-	`sha256:a5307b69bcea890e01277a0edf1000fe58566ef3851394d0343ccf9aaf02d25f`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5664f5f574a3b6f6fc10c85978211839f26fc15484b8245366f5aabe9eeffa2f`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 14.5 KB (14538 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d41aff4b3178934a34ad0776cce8a41aa1af20801dc613725b240e53054d9ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240754850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9289a220ffafc38840d72a9ed5189a93d996be3b238f8e5f98d601e9acc3d10b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:25:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:19:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:19:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:19:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a6cd9ce9367000978e62d727341fdbe8bd162e7346e254771317696df2b498`  
		Last Modified: Sat, 09 May 2026 02:26:34 GMT  
		Size: 133.1 MB (133110215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25b82eeed6d58316b0fa0d7776c0ebbf8d5d4164eab7632e6a1481028f4f64d`  
		Last Modified: Fri, 15 May 2026 20:19:59 GMT  
		Size: 75.6 MB (75565534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35197f4882da283c95f35061f0bfbd7904412c9ee9d74ac25c2d258e582ca4f`  
		Last Modified: Fri, 15 May 2026 20:19:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8d68c922640f1dbf8897284c037ee339799b71f6bd8a68dced85634376893cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f582bc7cc608f5dbde38c2db56925e2b2e22825ca224ce4428cb885a9b308e4`

```dockerfile
```

-	Layers:
	-	`sha256:209d23a53c3db8779625b3fde36909e5132615a11f57c090e7c8ed6c1d88ee1e`  
		Last Modified: Fri, 15 May 2026 20:19:57 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648938245746ac2bc80f5c21f89d0bec61daec25df1d518b88e7337261cc9df4`  
		Last Modified: Fri, 15 May 2026 20:19:57 GMT  
		Size: 13.5 KB (13514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5989441d4b7a1bf5101cc74248ecbffee30cee7e1f89b0edeff1891c99e3db3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222087729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6eac64752a0b78d5af6b96d7c722e453efe914e471f4144a5004667f1ab489f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:32:15 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52372d5fb2e4448599149f5fdd18e1d6933ee7757f50701f6b69d3caa03696a`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02341162e60f71a363777fc783abe7b13be75640bf77ce5850fc36e1883925a4`  
		Last Modified: Fri, 15 May 2026 20:14:12 GMT  
		Size: 68.5 MB (68543761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7264922cb08a03539a1a09b3ce8dcb79e62402cfa2033a0a48b49efc5ef33cc9`  
		Last Modified: Fri, 15 May 2026 20:14:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96da8efa55d12f979ae4f8d16ef0c4834f9fdfec829a16894c3216c317ede58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d379b293727708712161d6002c5624cc04f5ec4159ef27d6afa6693f0fb749a`

```dockerfile
```

-	Layers:
	-	`sha256:87a62580945f2b39cab34663df852d25ad7dfabcd9e8d8315334e167fc5d7725`  
		Last Modified: Fri, 15 May 2026 20:14:10 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee617d91d15f4d8b1ec675ddaf2d1787f6d0f01d95e6cf78c386d8e2e3b9dbe`  
		Last Modified: Fri, 15 May 2026 20:14:09 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json
