## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3b7e9a9d2b08144d1ac81f861a0358fc10951a49c0fc8fe8ac4259fb5746a8eb
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:73a47e9832f214fa30caeec5f22afc40c33e3a221c7386db51813b4ba703b3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243857752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34cf519cc26efe6c0f740fc35b0dc158baa357a0eba4ecf85483fafdcaa0a91`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:57:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:57:01 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:57:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:57:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372883b826fd5731e711eddc89d77333577a959f3bbcba15dbd7de321daf229d`  
		Last Modified: Tue, 19 May 2026 23:57:33 GMT  
		Size: 145.9 MB (145886244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d73e434f425d6afd7c8087763914a1202c34d46af7a7bb8fb58a0200702e67b`  
		Last Modified: Tue, 19 May 2026 23:58:09 GMT  
		Size: 69.7 MB (69737318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71bd6351aabe9b593997c7ae71862810fbaa3a45f39de84ea47b76e8ac814c`  
		Last Modified: Tue, 19 May 2026 23:58:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a8c8a04147541a16b194c110bf908bf700c50b25f05143f9b54a1624372ab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8cd2141113898a2003f3ce2f54afd101b568614aec444fe5b6a07edc8af499`

```dockerfile
```

-	Layers:
	-	`sha256:b54a8f67014deac7cf77d19b8bedb79443724a1e7c9e74370dca46a2bd5db2c9`  
		Last Modified: Tue, 19 May 2026 23:58:07 GMT  
		Size: 5.1 MB (5136330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4df9291f536f94134d7c80ec36138b28ff4dc4a64cc4aa2d3db4df4ee191a83`  
		Last Modified: Tue, 19 May 2026 23:58:07 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:086569c9f215c598dc73d907a463096d0d6dbef663f7a9f9d8f626647098b165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240429444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8988bd450d3f78d43ee46428c3590f7accd35acdfff71703138578f3a9f075ad`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:05:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:02 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:02 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d03745361f4539c228ec7f8a16d5983ebbc7bf646ad4386046a808d7d57b15`  
		Last Modified: Wed, 20 May 2026 00:05:41 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d3b9c8e18648afa8621dfb97dfc3101ce48648c3418230a8e85ae8f9715913`  
		Last Modified: Wed, 20 May 2026 00:05:39 GMT  
		Size: 69.7 MB (69731525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0177a54897b9736ca0f2c764a15c76c87c3bd50076c683cf1ece89d3386ca8`  
		Last Modified: Wed, 20 May 2026 00:05:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7e197f2f141d3c16fc7fb6f37dbd6007fdc5f78e108705e77ba19dd5e4f6a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce612e69491c6cc900fc794f2e6e6dfbf05a4993318c09bb3a375b4af9271abd`

```dockerfile
```

-	Layers:
	-	`sha256:f3931d3d63e083e39fb18189a1f8428a39121c004d200ceb78cec33f3bfb12fd`  
		Last Modified: Wed, 20 May 2026 00:05:36 GMT  
		Size: 5.1 MB (5142709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6020f2004a8662df74a491867424e74449681ebd03bab65f1449e5a990e4b931`  
		Last Modified: Wed, 20 May 2026 00:05:35 GMT  
		Size: 14.5 KB (14538 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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
