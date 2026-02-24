## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8841069f66bd5e2bbaaef1af28cf457320c4c126cb249a7193ec8d37624b9bac
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5a13aef0e0cc4ea33ffd07046c4f84cd68b87a2f0bb0581cd4092b8e7df3745d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275446699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f0bfa41ae9486b07a946baa9e97a36bc1a3688a5c10337d86aae78845537d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:53:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:53:57 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f45476e2176dba97ebd3d3471b969e8cbaa5b516f4c6fee0f55cf6595056e1b`  
		Last Modified: Tue, 24 Feb 2026 19:54:35 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef7aef6243d4a2f92d60a394bdf19d360f674373468c4e854afccfc5b9c046d`  
		Last Modified: Tue, 24 Feb 2026 19:54:34 GMT  
		Size: 81.2 MB (81150523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c259d1c774cc15bdba9fa4efe2d57a0255f6198bc26e9757a859dd18267bf6`  
		Last Modified: Tue, 24 Feb 2026 19:54:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:928e52aa0a1a35e01c91852437ab04df7b877f6b3ef3a0b2b21639540980a9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8f1b02257578fa23744da7d61a8d4aa783c3cee9c1fe57765c3e4784d04c9`

```dockerfile
```

-	Layers:
	-	`sha256:bbae26c98135a585f5a06da9ab8188b78e31b10e49dc91c8ebf3dafa9f2bb23a`  
		Last Modified: Tue, 24 Feb 2026 19:54:30 GMT  
		Size: 7.4 MB (7396930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cf59392c5d4c4c02d45fdcaaa90b5971379c6d11eaeb5243ba466cd783e7f0`  
		Last Modified: Tue, 24 Feb 2026 19:54:30 GMT  
		Size: 14.2 KB (14207 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7def8e2afac9214d185b05c594076957c0621bec3db26e282dfe1d6e2540edfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272013284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d211d3656c4171ea3e3dbc9318775940df71ef63fefaaabaab24118b7328bdc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:47 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:47 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcd013f701724f686e887838fe71684d11389b4f7e502bfba51c273a6364f2`  
		Last Modified: Tue, 24 Feb 2026 20:05:31 GMT  
		Size: 142.5 MB (142501416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8b20b1a60026ec984d164ac761f66a94103c0360ef3007634427e49a6faf80`  
		Last Modified: Tue, 24 Feb 2026 20:05:29 GMT  
		Size: 81.1 MB (81138016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3134d9fb96c170742fec767e529b3fba55a4c54159c225f1d1da6cf26203eebb`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:27df4c5acfce8c5361c76865f8108e828e9ea1c604f2602c6979b5de869fd0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580008ab2291e3db4311c2971e8e972dd0fb4042e35a526ef648e0c4425010a5`

```dockerfile
```

-	Layers:
	-	`sha256:c85e28fa0f2ece1956844d057686d313aa9928080ae37d4c300158afb73743ba`  
		Last Modified: Tue, 24 Feb 2026 20:05:23 GMT  
		Size: 7.4 MB (7403311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ece7ba8c486cac0a45f7216f5462b7c7f6e15142ff0527155a6f9e5653ce99c`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa557823a35ed62b6f176b21cee970f391989c19f5c40941b9305b5ebb19debd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272312522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60b46fdeee23d719c0f1f755fe995cf5c8f396172cb7be921f7f6012471e9a5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:33:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:33:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:33:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:33:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:33:19 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:39:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:40:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:40:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b47947f163eae116857a151bacee4e62eeef47f193f3d24c01851afc3df70f9`  
		Last Modified: Tue, 17 Feb 2026 23:34:52 GMT  
		Size: 133.0 MB (132997795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21adcbbc74d071ce1041ac188506348cb20b9320ad8082cc985edc24157d52a`  
		Last Modified: Tue, 17 Feb 2026 23:40:48 GMT  
		Size: 87.0 MB (86986790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ca5f3ee47d928ab3440771ec187f3c3cbacf24f840e23a3f960105ff5d4f50`  
		Last Modified: Tue, 17 Feb 2026 23:40:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:092dbbad7925ca62b6d8634d2ccf5f3449379653d66487cb74d8c49e815c50aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d96872f3f2f80894d6d4f134f47345e83a40e83d52715d5b7d66cd2f2161c`

```dockerfile
```

-	Layers:
	-	`sha256:b65362ce3e6c4263e5546d3f57b8fb21e9c9ffea3f03881838eb27dbd1f966cf`  
		Last Modified: Tue, 17 Feb 2026 23:40:46 GMT  
		Size: 7.4 MB (7401531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4ff4ec53a758753dcecf48cf37ff9f1989d560da5151819e2af07c848dcdc6`  
		Last Modified: Tue, 17 Feb 2026 23:40:46 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:640fe8c5038a3507480d2e280aae4932aa2e3915a1e45dea1d147fbb97cf9e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253664770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fa85b0a9c56e0bafd4fa5aa256b049fdfa555f04963d3170bfa6e83f5ff01`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:02:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:02:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:02:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:02:55 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:02:58 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:03:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:03:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:03:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feb4062cb5fc4aa1bc99f60bf8f1c09cbc97059bcc21805399a29e6bf55d62`  
		Last Modified: Tue, 17 Feb 2026 22:04:15 GMT  
		Size: 126.6 MB (126562060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1763f989184213c248c0ed564b39103051425cced6415fd4f54b98328c4a2bf`  
		Last Modified: Tue, 17 Feb 2026 22:04:14 GMT  
		Size: 80.0 MB (79963721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7fe2aa955052786a61ef6ecefaca733913c246e4e843ebc1c97dbf02176a0f`  
		Last Modified: Tue, 17 Feb 2026 22:04:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d38655df092ea1fb5b5046a17e949a55653ad42caaabf8d352daef1f687cb919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3847ae6b0441b89a1fa1d0a294b0fdaf76846bc4b19551d52c3b4cd4388310e8`

```dockerfile
```

-	Layers:
	-	`sha256:6afa874007bb871dcd4e8a76c547bf03d8594945437265138edfee5cc18b686e`  
		Last Modified: Tue, 17 Feb 2026 22:04:12 GMT  
		Size: 7.4 MB (7388253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203de1c3c7ca64e184a03878b0e2eb914bfaf94404019ce8f617c9ea7526e8c4`  
		Last Modified: Tue, 17 Feb 2026 22:04:11 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
