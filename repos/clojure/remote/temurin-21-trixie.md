## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:c48bb15fc085eb2063661b5b545d9376f716af34372c8e442095b4034b319a09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fd0f09038c82e775df8a6ab4f6100be0297049d6f62452dd16c0f0442d140067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295105241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca36696b578e1d59c18f1859fe9b64778cfd12eef5dc1d3b91427349199e824f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e489af8d54ef42e93ac06bfddc221ef9b10acf2d070e52cbc4d4960272605b9`  
		Last Modified: Tue, 03 Jun 2025 05:16:51 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf497c399295f480064eb295cdf2be27aa86e70a46a113fc9c96aad30fc66071`  
		Last Modified: Tue, 03 Jun 2025 05:16:50 GMT  
		Size: 88.2 MB (88222800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed1d71bbc89cc763d1ec0d84c8e93f59c2bcac08d35ec7ced999ece3e6cc66b`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc8c19475b6deefef99541c8e184b5bdb1e3e8d56f315cf0022e2c4f545e83b`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:077d495346f38f4ae0edf5001e83f62748fc2e1b6ab47e23d4511b43945763d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd5273bfdaaabe59717b3f1861e0f3bd7cfb2176be4e55d702f506874cfb276`

```dockerfile
```

-	Layers:
	-	`sha256:ab3108e6577e71371de471c0c7e7e23766a17fd5f88ceb174db2eea8f9d8787f`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 7.3 MB (7322186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a5e35efe6ca45c2d88f1145d38a874b28840dadd9b5f9d1433665fdbc50867`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b983e8e9f82f9d7cc3ea752f1fbd50c201aa93e98b2cde01ba6b5500dab6904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294053999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077843ad43fda4ea4564624dcb4ac66393b67d3fae8ee78dd7c5fcb157bcdad9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669209475ccf588005064aec8b03f795116e849de02f62977a14a87f1ef3e90e`  
		Last Modified: Tue, 03 Jun 2025 10:57:10 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6277af476c426cccf4b08a5700f8ecc9ed2421b3d5c41ded25b5fbc46f47a492`  
		Last Modified: Tue, 03 Jun 2025 11:03:06 GMT  
		Size: 88.5 MB (88505834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e4a51566f9b77bbac95691db3f0859f7bfefe6acae0fff55cff3b58362e18`  
		Last Modified: Tue, 03 Jun 2025 11:03:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8386f8eab2bb3a254e814e6aca6d9c87f4a5503bb1e23e92f9174519d4cc87`  
		Last Modified: Tue, 03 Jun 2025 11:03:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c4f500dbc5abea4fcb9e9ef9cccc3a3380df2ce3d97badaeb4efe7f5eb64b4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4c8c3da3c756134609cde198bc4eb1c8a2041fd6c84adf73cc20efff8652ab`

```dockerfile
```

-	Layers:
	-	`sha256:f059445ab874807e778ddfe5202e7f42165fc7f2a7cfb6d43f3591ab3ddf9a98`  
		Last Modified: Tue, 03 Jun 2025 11:03:04 GMT  
		Size: 7.3 MB (7329240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7732f073f5924a8558e1540cb4498581bebc6c5e9a03474c9a1629dc942dad79`  
		Last Modified: Tue, 03 Jun 2025 11:03:03 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b97b4d759fb8c79faabb05aa2e82af8cba36b16c9cd19e9dc6b2764580fdde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304843476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7ffb99954424ca4a39f48403cbaf889174120ca3e790cdf397ff429ed37b8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6bd552c8941351aec1fc10e7be3cba78443c32cad3ba1481c6ebefe465a52`  
		Last Modified: Tue, 03 Jun 2025 09:11:02 GMT  
		Size: 157.8 MB (157804856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41445e119a9a0d9c4a0bc7968957eddee821e74bcfbaa3eb26100bb70d38385`  
		Last Modified: Tue, 03 Jun 2025 09:21:35 GMT  
		Size: 94.0 MB (93957040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a449e68393eef9a1411755732e3e40a68a5adb3f15b6de294483fc737365cbfd`  
		Last Modified: Tue, 03 Jun 2025 09:21:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bee6042962ce03b80806fa4f4667d7ef78e7889243c59d255b516380c8592b`  
		Last Modified: Tue, 03 Jun 2025 09:21:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:137091a6262c0468795e928ef5911d5f667dfec4de8538c9e6b8444dc7053ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049aa3c948a4c62c0fb15b63beba99d4cb4b00d2d8e9f4dd90bbdc5e7c1f11a`

```dockerfile
```

-	Layers:
	-	`sha256:4aabc5886245506bd2ab1257524604c7398dc3b39b77b22db8ce7809438e6f4a`  
		Last Modified: Tue, 03 Jun 2025 09:21:33 GMT  
		Size: 7.3 MB (7326615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b496d68a40c8aada7b147fd65300a0631fe2e560fec995e2cbbd7715fb477661`  
		Last Modified: Tue, 03 Jun 2025 09:21:32 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:fa4d0fc49036a1adb6e12d1f99b2ff02781e3098b28d9cb7c51e0edea7bb3569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288022498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb70c728cd256d73ad2c7fa015e725131d5dc878c007348b29e304f468391414`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df655a63a53f1eb7344d055b3a0a02078ae226dc1a077e6b3a1117732b72b764`  
		Last Modified: Tue, 03 Jun 2025 09:38:50 GMT  
		Size: 153.4 MB (153449622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1575bedb9b419f39892e40f3982cc97f8e65e7ecb687c8d0dc9d3818e62a9`  
		Last Modified: Tue, 03 Jun 2025 10:02:15 GMT  
		Size: 86.8 MB (86840425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f36ff33de9a6eee5453014c525180ea55b72f1ddec8bfb7febd1f2dc7f582`  
		Last Modified: Tue, 03 Jun 2025 10:02:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6ef0035c620bc72e9894fdb40140b710372e01a9a1c69cbb05bda88071fda6`  
		Last Modified: Tue, 03 Jun 2025 10:02:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:096be60b94b028ff1bc3ea454d39367ca3f153bd0b7cb7d59d1c0068cdb5750e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65c5e18d1babb4632fb18d50801a65706e66e72a0b20954c848005188dde07b`

```dockerfile
```

-	Layers:
	-	`sha256:9d0d76356310e5dc9d69c8314fa24dd169d78892513c57eda794bebcd77c5ced`  
		Last Modified: Tue, 03 Jun 2025 10:02:03 GMT  
		Size: 7.3 MB (7310109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621e37e87405a55d9bb9371ea5050444bafda1877fee781c0f43ffb2e93f794e`  
		Last Modified: Tue, 03 Jun 2025 10:02:02 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b21281a6567a866971a58bfb08538445ce39837f640af5a844f220917f65ea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285185666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9229fd22f69f90a73d67a0fe1d7f4221368963d6de40f59ada83d5ae3afa3c95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861de86bc3adcdc8dc3323ae415856608e017573655a6d8e472b10aef094a90f`  
		Last Modified: Tue, 03 Jun 2025 06:28:03 GMT  
		Size: 146.9 MB (146911014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886b8856d641f52a0291ed1ef7c5d3a43538bf606ca8af9e36a0e70ccce4f06b`  
		Last Modified: Tue, 03 Jun 2025 06:33:38 GMT  
		Size: 89.0 MB (88951385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084e5edce2067ac9b9c8ae2644bc30afb974d105fefec5839bbb4e85373418b6`  
		Last Modified: Tue, 03 Jun 2025 06:33:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2ca26316467dd086cd23d495068338cc7e7836e967e3cf23e9dd2057b3ce2`  
		Last Modified: Tue, 03 Jun 2025 06:33:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee6c73a73cd75c456da44879c44caf311465dbeaca0f6388e91c1cc6d8cde2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5346553b240908f36c6d642364852c8bb75560550b5b0c60b6b3cad2d552d2f`

```dockerfile
```

-	Layers:
	-	`sha256:d443a4218b0bca92efba3165271a90b0fa278de5855b1edb6275e8cc56f1ed2f`  
		Last Modified: Tue, 03 Jun 2025 06:33:36 GMT  
		Size: 7.3 MB (7318108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3389466fd8326f61dd6adff0f31d27ea14bc2aa51355d1a8f9e872d063b8dd`  
		Last Modified: Tue, 03 Jun 2025 06:33:36 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
