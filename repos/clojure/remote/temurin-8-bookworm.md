## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:4b6ea366a67b65c49e04ede829b39cdff1def6737063857d29ee4fcdeccfd70c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b8e607fc9412aa5fb618a8645989aed0d875246f1932bbe26e866298de6b91d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06ee6551226c933e06ccd6d9b812a3b985e63dfcccfd997f7bf792ccf19bd71`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:49:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:49:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:49:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:49:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:49:50 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:50:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:50:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f355bfeb2a326a2f549d5074a71ff615b41439857ac7d0922b063673bd1e7d93`  
		Last Modified: Fri, 14 Nov 2025 00:50:37 GMT  
		Size: 54.7 MB (54733366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b8678aff2da54917f0b84bb8c9d433fd49504c6a37c0e6709a2da0df466fa`  
		Last Modified: Fri, 14 Nov 2025 00:50:34 GMT  
		Size: 81.1 MB (81146209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a38a776e1687bc5206c62a2566255f2180053b2de793e853c697ca4f62503`  
		Last Modified: Fri, 14 Nov 2025 00:50:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d855b3867c55fb481c13bd1be55cdd4fcd6c7f973bb5a031a185621b530a096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2691591b008b182ff4ed1a7dca895ceb94963d63fcce20564d65cda76cc3b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f9c1e1fe3b74e1f6079f54bd46e1781ebc4d55250f59d09fe7b813ff46f23dd`  
		Last Modified: Fri, 14 Nov 2025 01:49:09 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65dcd688fd848550e2c6d73bbf480b415c4f54cbe19421a8fd3d55fa95a6a4c`  
		Last Modified: Fri, 14 Nov 2025 01:49:10 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5e587ad2d60d250879ae0b17a4dc5c0bea033f5186e16cbcff2cca320c99151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183206489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d88ca538a57372376edb2ad73d8d42eb1e0ecefb64ca200406b40b0a0a4cfc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:51:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:27 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f275fc141ea56bf7987d637682ca4d46638dbfac59664e75f6cdf1467f6a1c`  
		Last Modified: Fri, 14 Nov 2025 00:52:13 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb3ed28953635dd7c451e8e22e73cd205b6e641a0d88f024c8ff50d9624c57b`  
		Last Modified: Fri, 14 Nov 2025 00:52:16 GMT  
		Size: 81.0 MB (81031368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a1a63d2943099ef85da7e3479bd0f5d82cf9b56bf913f1cf0822e8c153fff`  
		Last Modified: Fri, 14 Nov 2025 00:52:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0f912572ee814e31ba445dedf17550048f0f73e61ba6437ae7485aaaf868da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070117a6d339847a4681707ae920460d1f327ec699ec3f331c38dac5d513b6b9`

```dockerfile
```

-	Layers:
	-	`sha256:9cc5f2fe6332ff2f837ae7cbe908eb1949c1dd2bb93bd18493c4aebb3ddcb1e9`  
		Last Modified: Fri, 14 Nov 2025 01:49:16 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48bb2ab31994177063f7b29dfa863b6d9aa9e40be5effdbf5a8ca266db2c4fc0`  
		Last Modified: Fri, 14 Nov 2025 01:49:17 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:13f07fac92a870a34bebfb576a27c23e146aa2d940fd65c636716fa8d2c62f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191489083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7726e0afd58efc0c8a1e2e245a20f394fb75dbe23ee9d4cea8aa2ab1eb70f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:07:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:07:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:07:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:07:13 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:15:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:15:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:15:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d32be4fa3f3f6cb4472d405863e8c9515baaef78e3e54ebe7c4f01ced5fc4d`  
		Last Modified: Sat, 08 Nov 2025 19:16:12 GMT  
		Size: 52.2 MB (52175124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65204b4ead1c81678cd2d4ff6ec14d8aca8ffcf14189cc01065d3bd28178562b`  
		Last Modified: Sat, 08 Nov 2025 19:16:15 GMT  
		Size: 87.0 MB (86986035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4485a3f68c0cd7527310704381bb1b915f1eb1fdcec8c157a2f2ec85fa84502`  
		Last Modified: Sat, 08 Nov 2025 19:16:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fd43419ff2ba6dade51691877641305d2fb87af8fd0c846a9c46694caf2ab58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215573f3571c4c6e3dae64c2c0cad0b292440a06dd2f95e96d2069ff4f1381d3`

```dockerfile
```

-	Layers:
	-	`sha256:ab684f0ce3ac36bcd680b0a9ca0cba2d2919216629fdd31e4966b2ca08a971f7`  
		Last Modified: Sat, 08 Nov 2025 22:54:09 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b1e9d35799d6d837878d2ae4f3e7d2e7da5f4755ef7b4020e2ec5281137edd`  
		Last Modified: Sat, 08 Nov 2025 22:54:10 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
