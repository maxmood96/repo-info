## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:927990f0c4d0dc86b9ffc60e2305553685f5218a4164ef51c9c7be2b41b69d57
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
$ docker pull clojure@sha256:85514d51faa3d3070606758f39ec7669b3b4fe054347b91a7badffe2eea2ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240758509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad466fdb7975b1f75516ebd7e2c62381f46b0569dce5abd26f2f4de558930ab`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:48:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:48:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:48:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:48:27 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:48:27 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:52:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:52:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130a767dc3bb77d8ed9ed1426dcbad9873738eb6feb4a4b9929879d8a40136b`  
		Last Modified: Wed, 20 May 2026 05:49:51 GMT  
		Size: 133.1 MB (133110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb651e05efc2631c6c018e99f80cffe1df2e816e5899c31bbde1b1942fa690b`  
		Last Modified: Wed, 20 May 2026 05:52:35 GMT  
		Size: 75.6 MB (75571927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ce021c76eabc12145576c11a4adc435a911ba0f458a36ba51d17605ed1226a`  
		Last Modified: Wed, 20 May 2026 05:52:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2757713e6200d2740bef49e9057b37b6b9595e0926a9f097e8bee28fed944aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b46f9f7f5b39d5dd596c1e259570fb6ea7a667f689aceee14140aec13b4545`

```dockerfile
```

-	Layers:
	-	`sha256:779405969738786f5536867555f18a7e2566fb34c75f3af4c1b7aa864581654e`  
		Last Modified: Wed, 20 May 2026 05:52:33 GMT  
		Size: 5.1 MB (5140873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af73ae16c93d797cace2cc7d64f821501e1c7f0bc8ed754dec01cc9edc42d05`  
		Last Modified: Wed, 20 May 2026 05:52:32 GMT  
		Size: 13.5 KB (13513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9656615c226f66163cba89154687a8d8d6ee9a2d9b5d0a238cbc97c6d29c2501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222080185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfacc32e203fbcda132fc79717eb37584b60ee63c2c7225852f6dc8ad348d7ee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:41:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:41:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:41:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:41:36 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:41:36 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:42:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:42:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:42:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6016d4ebf4c94d6542085c791df63dbd93201c2c8fc6d05dc6abacf51ce4a`  
		Last Modified: Wed, 20 May 2026 01:42:15 GMT  
		Size: 126.7 MB (126651716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8d60a2e9b148577ad76b0c08d38d4b801c6f69b7996b432885242579ebe243`  
		Last Modified: Wed, 20 May 2026 01:43:12 GMT  
		Size: 68.5 MB (68539229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10e048e79154eaad170cd904e2a2adbd1b46d90f6cda7b45396ac2e9a32962d`  
		Last Modified: Wed, 20 May 2026 01:43:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99d83b718b4d711a29da8d1a250cb562364c357543bc97945b445a3c563d1df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa0d9191a5216ef6e900bd47306dbaa1cd4fcaf875f000813f1aa4393eda28`

```dockerfile
```

-	Layers:
	-	`sha256:8b26553babdcede7f117251f5008505cc5f84994a86ea6045fe8b843dd1c64ef`  
		Last Modified: Wed, 20 May 2026 01:43:11 GMT  
		Size: 5.1 MB (5127655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f602249c00aad629e5cd0012580425b3dba5575c0bda293498f0f2954d852b63`  
		Last Modified: Wed, 20 May 2026 01:43:11 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
