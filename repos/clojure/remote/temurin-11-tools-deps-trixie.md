## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:30acface6b64a9136c6241a04ff6c517fb5aa7b7679de910571262d99eef7c17
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
$ docker pull clojure@sha256:786aadd81dbcaf3b498d12eabeb258a3ce3303220b5b2acb03f7ad418270e803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280642126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf92577b0db4c49f4048af452cad807c9a4ba30948ddf91479dbc2ad2ea7f1c1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:24 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151031c9591035b7ccccbc73fe72fd16d8f997d4e160115b07008d8426e17ed`  
		Last Modified: Tue, 17 Feb 2026 21:43:05 GMT  
		Size: 145.8 MB (145806699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423b3e84920fab0e84cc1b6096be03d7cd43e27d502ada534ba6adf90ee19ab`  
		Last Modified: Tue, 17 Feb 2026 21:43:09 GMT  
		Size: 85.5 MB (85541830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2df90f8a162a35400be48771a6e7a4748fac43996ed4452fcf43f2e3d9800`  
		Last Modified: Tue, 17 Feb 2026 21:43:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2ee22f981d588b3eccaf1e0fb341fd3df6f23ddc3e5c99344c9c318e3beee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cadc0773c143d38079ade4350fbec0feabccf02d64c37c5938f3450be5d0c1`

```dockerfile
```

-	Layers:
	-	`sha256:6e41b66a710870046da5cefabae96c3955f749cb41fd8c8f97137580c99b0cfb`  
		Last Modified: Tue, 17 Feb 2026 21:43:01 GMT  
		Size: 7.5 MB (7489221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f0ce8d72adbf050f5233266abf4b521f4525a8ea86b9c0fe61fc17d86a7ac7`  
		Last Modified: Tue, 17 Feb 2026 21:43:00 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b2c2bc67f31af4ae46129c3c4b3eec4d8e88603d19d0975fb4548fa2c7efb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277515699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbeb4751b9547a2574a026cd604a1c491758d17cc41ea3791f846343d0a7632`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:42:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:18 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba297ef4cbb3dea8d1319481ceff7dda59c6d6cf89471d29829e078e1cde08`  
		Last Modified: Tue, 17 Feb 2026 21:43:02 GMT  
		Size: 142.5 MB (142501413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641a73096f4282ad48206de54c9ce32a1fbe749fbe008d12b7e8f481bbf36bce`  
		Last Modified: Tue, 17 Feb 2026 21:43:00 GMT  
		Size: 85.4 MB (85361622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36d76b8e922efc68b1743435571f9d9d35a766fe2ba3525e1d403e722dc2271`  
		Last Modified: Tue, 17 Feb 2026 21:42:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:417e4e4b522ab773c180b0d042de5073e50d0145e613af1483d6d62a006aabac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4f8ece190361c351b6611310514b6484b7765da5abdd213b0a14b271009b10`

```dockerfile
```

-	Layers:
	-	`sha256:f14ba221527960c9a038fc8158fa78bcf24dc1008d850c17d927d4ae02a447b4`  
		Last Modified: Tue, 17 Feb 2026 21:42:57 GMT  
		Size: 7.5 MB (7496869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:719a6b33e5b29bd714f919872782ce283beeb7b1692a066bafbdfa8a6b86132d`  
		Last Modified: Tue, 17 Feb 2026 21:42:57 GMT  
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
