## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:affed94e6bf37ebbc916b3f9314cddc3d5aeff6ff6416aa4b28f7a7773a73ef8
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:79101f87e981ddb532f385bb01733631aba2782424aa2ac7aaf7bb29e062984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275457701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0faca33ea76c99c27ec92f3cf8786f43080ac5628f1a760ec1fa4636a100c9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:49 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:49 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef5ef1655a68fcfc0fb1590ff0bbd06d6142b68b474884806ed585d85846e96`  
		Last Modified: Mon, 02 Mar 2026 19:48:45 GMT  
		Size: 145.8 MB (145806702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdce05fb5068f7dea54d950d1a1aec26381bba4712ff7f4c8ae8eb69e3c91bac`  
		Last Modified: Mon, 02 Mar 2026 19:48:43 GMT  
		Size: 81.2 MB (81161577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb2f2aa4e69423542fee5f26d7b82c38fc2901c44cdb80fa2a9c4e30f6587f`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:567932963d362881b63b5c3b890ece7dc230cacb32e9b159c8c9069d488b2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce22d28ba7d809123df6067226fef4f9a69e6dec0d0b73a8c4b41ca6d3b8364`

```dockerfile
```

-	Layers:
	-	`sha256:789c35c6115db513072e87da235a966091a2a1e8a8a5b67ca057c201356a470f`  
		Last Modified: Mon, 02 Mar 2026 19:46:52 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc287956fad952cd3b2c68329d7185da918110eb491eb61200e37b8ff9773f1`  
		Last Modified: Mon, 02 Mar 2026 19:46:29 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a404bb7dde6dfca17e13140c78486d721141b631a6632712e12fce8eb19b9519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272030719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aee33dd363e2f2eea9ef789a6659990265c4a0d70daf9089015576af74bbd68`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:40 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:40 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4b9f67987ee58a7f248353cc1aa60d47898de1c0d1cb65ce6ff1dfd71cb03f`  
		Last Modified: Mon, 02 Mar 2026 19:46:19 GMT  
		Size: 142.5 MB (142501443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d0cc55e54c204283e22378590c1623295392acc85fb0087aa77d39a53ebb2`  
		Last Modified: Mon, 02 Mar 2026 19:46:18 GMT  
		Size: 81.2 MB (81155421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c915593097c574df26e1fa32c6a136992a0dc74b1dda331fc59a2f197712012`  
		Last Modified: Mon, 02 Mar 2026 19:46:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:25fffb97d4e734d6e4d0bdcea30222eba8a48a3fca2283638f6b8599c0ddfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a9adef7fe86bca8f08217b9330944db5017070eae6f95beeac4a5efb85dac`

```dockerfile
```

-	Layers:
	-	`sha256:3dd14366402b7689c7be03659bc61521c6d165d4f5f74771be1841c139396fa5`  
		Last Modified: Mon, 02 Mar 2026 19:46:16 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8fbbd739efdc3394b44355769d1fa5921f8e5426e239b10e6fd7b54c4c8900`  
		Last Modified: Mon, 02 Mar 2026 19:46:15 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c883d363bc35d7fd6adcea868f989fe88e4cf310fd114dc6f0c6ed4afc584a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272338643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc37d37c6084f5f0dd355a388ea269f5bda4aeaa2682f7ddacc4e36ddbf39b7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:50:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:50:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:50:33 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:50:33 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:51:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ac6b29431ffa909b639654113c493d029a977cdda0f77f5e19b0cc7ec8714`  
		Last Modified: Mon, 02 Mar 2026 19:51:57 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8663bb226ad20376c677bdb601d0e10af318011790c742cf5795bd88dd07fa8a`  
		Last Modified: Mon, 02 Mar 2026 19:51:56 GMT  
		Size: 87.0 MB (87003389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d800c461d13d54ba60bd7806ac0e0df0945053c4d9a522993997fa693a52bf50`  
		Last Modified: Mon, 02 Mar 2026 19:51:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:30f6e635d012d364f142a95fa593226b55f0c35cdb37b2b9a1a755817856dc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d48421045692a46ea04ebe2f8f7f78ca07781757e41a8952873af6786aa536`

```dockerfile
```

-	Layers:
	-	`sha256:5b6f70cfc857970b3fe5a99b0b8402c19958d72e3e10f83f5ffaa6e46f205f12`  
		Last Modified: Mon, 02 Mar 2026 19:51:53 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfec8c5f8756b6ddef9c01dbd872564db3bddb2dc0b989cca2e690fbb6ca0ada`  
		Last Modified: Mon, 02 Mar 2026 19:51:52 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c804b578d20fd321837c8ffb950fd6fd5d9754c46ee6a0c9846398fae2ef086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253685516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ccd5bb1b9aeb8a26f577b4247191b784042c673046afa5520d2f1b4f9b6552`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:48 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:43:49 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:44:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:44:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4516a3d64dedb36867dfd0370b4c147205b1f54d4118dd32addfede7f46972`  
		Last Modified: Mon, 02 Mar 2026 19:44:38 GMT  
		Size: 126.6 MB (126561998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d7a53b55b19bc78628f9a5d5e6aa98fde7ad323a92e19c7897b29169ded509`  
		Last Modified: Mon, 02 Mar 2026 19:44:41 GMT  
		Size: 80.0 MB (79974786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d282421892380ef4c500ab0cb2f452a4c180bcd2cd1ae00955ce5b66ec33ba4`  
		Last Modified: Mon, 02 Mar 2026 19:44:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:02236a6b9c53259e98a4e012afbaeef3322f5635c324763f0dcbde4f82137ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230d98f3633f0288755a635b624ffa6ae944d5cb2959301f799d1d331287c3b`

```dockerfile
```

-	Layers:
	-	`sha256:575790d6684328462aee01ca541c34b68551af7ed960dd7f7e3acab45feac84d`  
		Last Modified: Mon, 02 Mar 2026 19:44:39 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5971cb10199adb85194e95e369e02efb831bfa99147c88b867721d24c82b6671`  
		Last Modified: Mon, 02 Mar 2026 19:44:38 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
