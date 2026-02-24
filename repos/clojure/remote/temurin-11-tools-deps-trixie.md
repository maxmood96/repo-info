## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:2334f185d5c29ae24c9fbb29fe6eea8723b09f89dd8932c6f477a07b711ca18c
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:87a7204b521893dfceaecad3244d8401ad4ee8265909733adef781a060da7ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280640534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761891f32cc70cace142e29980a141dded818d0f831dccee3e2fc1d059c98f41`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:27 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf008242c67674e4b5f31f9239f06401c7bf0e3a604f4adb3bc3b61cf6e93f6`  
		Last Modified: Tue, 24 Feb 2026 19:55:09 GMT  
		Size: 145.8 MB (145806755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a30c463f6db66e92dcb7b342c7b3c8e871a7141313940f9738b087270f89cc`  
		Last Modified: Tue, 24 Feb 2026 19:55:07 GMT  
		Size: 85.5 MB (85540012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc5fc932c6e6f59bd6a9985d3e5c7fbb4a369ccdb0b13a1abd0d8f211d4d5fc`  
		Last Modified: Tue, 24 Feb 2026 19:55:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0ed8eda7b4c809ea17a9ef4630fd0b1f2923b5f57a268ccebbbc390c99350308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbe997f5ec2a993f26e4999ce7a359ecb711d73c591af554e3445c8b04b10b6`

```dockerfile
```

-	Layers:
	-	`sha256:bcbd34ec3039ebf324ec8cbc2e5273fdd6e0a2b82c247354e34c2f9e6523e41f`  
		Last Modified: Tue, 24 Feb 2026 19:55:05 GMT  
		Size: 7.5 MB (7489221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7545d70d5965d3930d4519d45f107d2d65023c1178c5ed5f126848b1902c203`  
		Last Modified: Tue, 24 Feb 2026 19:55:04 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3afb0574dbeba0c6156202556a22a8fbcf4e3ee710dab87a8f1a8a22866414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277519100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee704cb4f4252cd9b4ab069a945a578e0faed11bc74faeeb6b78c4e719742f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:01 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51837a702ca51bacf6a9c26ccd8663fe8ab5764d31f01529649aad1104baed6d`  
		Last Modified: Tue, 24 Feb 2026 20:05:44 GMT  
		Size: 142.5 MB (142501443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab6d49d50a3eff93bfa6c033b7f0bdcd2c00d37e31d3e648f62bad3e6377452`  
		Last Modified: Tue, 24 Feb 2026 20:05:43 GMT  
		Size: 85.4 MB (85364847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b985bf43a004938f27b09ffc01c8eec6fe06f592f4e620dd31568f2b7fc76b`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:79983c861546e074ff552af699de92dd7b2e06bb0f2244b4f7e7294ab38145ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cfc07443f44b1e8034cdb182e088214dc3dda6f6552aef44ae8c7a70e991f3`

```dockerfile
```

-	Layers:
	-	`sha256:e5e596634d735c2666b642365edb048e8fbd91ae1a5f2a57c4ff4ae5c61f79f4`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 7.5 MB (7496869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556776dd7e8da2d8f23b74896fa70e659d52cba0165cf29d25565472ad856de2`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b379c8c72d4d8cb3f9906cae831da49a08f35449cb38e4e013afa9f692c8cf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277058178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52245722ac68494c788c95cb1f297f3a316829193070dd0345246cf3272625`
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
# Tue, 17 Feb 2026 23:44:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:44:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:44:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ea58df9d5eb840d3ee88162e3f67c2743c098ce80de629ce328e4ca1f7bf22`  
		Last Modified: Tue, 17 Feb 2026 23:38:15 GMT  
		Size: 133.0 MB (132997814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004cfa4c45e87e666612541b311e7decd427d85471761978c07bfc5cd946024e`  
		Last Modified: Tue, 17 Feb 2026 23:44:51 GMT  
		Size: 90.9 MB (90947603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8696316bd6d599028d49d79bd41dd77182baac79a0b45cef3489a82c2f340b4c`  
		Last Modified: Tue, 17 Feb 2026 23:44:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb0fb1347c1a622d45e8851701fcb528ed3b7d02d8f30a70ea2944d878ad7622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebfed6c9d5bcba6a36855d081aeca340d297c62e0406c529588bfc16bc213e`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9ed9f354ee347b2f41b6ce081bd06cb6d8bc25c6dbb1051d792bd23271360`  
		Last Modified: Tue, 17 Feb 2026 23:44:49 GMT  
		Size: 7.5 MB (7493027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7c98c2ea422fee2bce58206f706ff4a7d4c323938d747bd49e21dc94f4dec1`  
		Last Modified: Tue, 17 Feb 2026 23:44:48 GMT  
		Size: 14.2 KB (14231 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1294eacc2170c6aaecf7fce96a45f66696595311c50d6256a59e7096fddb632d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262428914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7726e5a078d2fc13c8482ec058926084879d06dc4f4d4953b40f167ff6c88065`
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
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4228042fd7c68977db9732b8db040ab2bd28f30bc9d5526751b817a4d24e5ef`  
		Last Modified: Tue, 17 Feb 2026 22:06:38 GMT  
		Size: 126.6 MB (126562060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f6d0102469b02401ebd875e3406bac28860e6a60e924ea6b891aac7d732a7a`  
		Last Modified: Tue, 17 Feb 2026 22:06:45 GMT  
		Size: 86.5 MB (86511828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b4d6a5747954e0784971257e4c7df36ac0e60e5547f02d09a7f25829d7a15`  
		Last Modified: Tue, 17 Feb 2026 22:06:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:064ef09346455755e89592c8f0ca63b69ab5aa501f9a3ea137748f2b5d4a0007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab95446bf64a3a582c0a12013673102a5660a9e988f6eb18b90158d3024d6995`

```dockerfile
```

-	Layers:
	-	`sha256:3252f6bbc1a716137ba0c13e8bfab731fda78db1a592f1c4cfd13dbb0764562b`  
		Last Modified: Tue, 17 Feb 2026 22:06:43 GMT  
		Size: 7.5 MB (7485147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e2068e3168ed7b6bcc901348d299240c61313acb3fbca3d958e500eec57d82`  
		Last Modified: Tue, 17 Feb 2026 22:06:43 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
