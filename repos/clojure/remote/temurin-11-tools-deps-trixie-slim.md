## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:1e08fdbb78cb14ad0c95625386b3ed2c57f76b9880cab695a59e5295a51755a7
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0dda55e26a39b87a90deb1886d04b7b982ee7658e2311457661b292f9196c475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247580208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e3f1da39a363f2352e6b612a92fe4f499d22dd14d1d3e93e6609c1b493a9d4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:37 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae567c9ad885cb8c13393c568a4bc37d5452a750d8ae7022230419e78da0668`  
		Last Modified: Tue, 24 Feb 2026 19:55:18 GMT  
		Size: 145.8 MB (145806749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9d796ada83e7a4bbe12a71efba33cb76d97f35da2f25916dfaa37cec824b0`  
		Last Modified: Tue, 24 Feb 2026 19:55:16 GMT  
		Size: 72.0 MB (71994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045e207aebe77015b7757c33e6044bfbdc65f804d8d526c3a7710c3c81b86bb`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a366e9465771a55a995443a7bbdf3e4fa66021c62b31e6b78dc1450c1691332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9809fb45d2fa46e2ba279561501d9a8e510c5eed30849e9604168b77190919c3`

```dockerfile
```

-	Layers:
	-	`sha256:159e9ed72af9b9e4d17e6bb1601d3c74c92bc3ff55301db8315e68248cd87a8d`  
		Last Modified: Tue, 24 Feb 2026 19:55:14 GMT  
		Size: 5.3 MB (5277692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ff53f0f65bf2a7c8ccd6e46d7d1a02ec2c20129b69592906c7c8a1ea2bcc37`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b492e699d6190771b7854aa233ef1af4bf72af6887f7c8e36e96f24944e174c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244450242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356bc63a5e72bf4a1480a66b0aeddd042dc861ceba780b5fb8eafac353804548`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5832d85a6c75b7379d03869322dff4323c39ae58f9e9d4d4344f20cd8de75c3`  
		Last Modified: Tue, 24 Feb 2026 20:05:46 GMT  
		Size: 142.5 MB (142501412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f29df623a2c45365fed7caa0c1c391a4df059b856cd43da52580eab3c60a36`  
		Last Modified: Tue, 24 Feb 2026 20:05:45 GMT  
		Size: 71.8 MB (71808088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11fb6add92ad2897e529c7bfb6783beadeeca1faba74153928dbd89a6510bf`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01d81e28bdf3d04ffc955d26cceefad0b167a9476855235aa8268b40d9f32b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700e409808ee81b1ca1dd4a49d03539a9d6fe60112877acec4bc7b17545e0936`

```dockerfile
```

-	Layers:
	-	`sha256:7a9e6aa65465a008b6c51c01c3e7c81ab428df5adabaaf3d25a9cc39a8195b17`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 5.3 MB (5284079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aff50fcc5c73a652f3be2087f74f2d82bcf5cf08751d2271bb725a63c58bb63`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1e2e36b78f7341bcb2f025d9071d8eba5d4432f65898f8d9fb863e458fbe103a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243988985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1a7aa8b5cefb38424f2d09bcd2145bba3336f5dab7e47a6885f743637ab99`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:36:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:36:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:36:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:36:32 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:36:33 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:44:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:44:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:44:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ea58df9d5eb840d3ee88162e3f67c2743c098ce80de629ce328e4ca1f7bf22`  
		Last Modified: Tue, 17 Feb 2026 23:38:15 GMT  
		Size: 133.0 MB (132997814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ee119024f45087d6133f4c886e3daae9ead6420ebf737dec88495bfd32945a`  
		Last Modified: Tue, 17 Feb 2026 23:44:47 GMT  
		Size: 77.4 MB (77390339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a240f46d2574a8d16c923b44d1e590e8fa1519a6c4f4e1793d67a79db255e496`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70dd82eadb11b503eb48df516d5049d6982d727e8b9b11e263879a0602b4b4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5295739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bddd069198efa497b2015be7310d83d7f592dc9c9634455b8b4d242360376d`

```dockerfile
```

-	Layers:
	-	`sha256:52359d3ba01f35ba0b5bccd652267ec20ad3ceeef24b00eaa451ce868311426d`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 5.3 MB (5281448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab524fc544a470e326721a4d89f3abac1c8673d50d6f1c33c0a5b80616e723e0`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c06cb07fc57b28fc8d729537c655466bb21fc3584e1bce203252f34df97eaaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229354013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811e952de955a981d46e9085d4cd31b1e994fd4c5eb2057db9e8d02d99a9e316`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:04:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:04:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:05:00 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:05:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:05:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4228042fd7c68977db9732b8db040ab2bd28f30bc9d5526751b817a4d24e5ef`  
		Last Modified: Tue, 17 Feb 2026 22:06:38 GMT  
		Size: 126.6 MB (126562060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518d12f377ce94aee4e3dbbd4baff57f061dd069f2b1d59aee359b3cdc471c1`  
		Last Modified: Tue, 17 Feb 2026 22:06:37 GMT  
		Size: 73.0 MB (72953155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c14f4be0ad73764e4d7b1977fdcd4f5b1f608237796c964fa61529724bdd0`  
		Last Modified: Tue, 17 Feb 2026 22:06:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f73b0a9cd895325892cdcb7755a6ba6c265611c72f0bb238ebf48d95bceadd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e80867fc07801857708a7e04ae27752718bfe2b2efe64ded8b8a23cebf795`

```dockerfile
```

-	Layers:
	-	`sha256:ec795bfd3799056da0adb2e4fe8d2a1931a31fc4de0e20943fdd216d48a59778`  
		Last Modified: Tue, 17 Feb 2026 22:06:35 GMT  
		Size: 5.3 MB (5273620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae02c02c0f2622eb0c34f39c760cb818947159b85be8fd391ee46e45420fd`  
		Last Modified: Tue, 17 Feb 2026 22:06:34 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
