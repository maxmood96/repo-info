## `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:ad366c71b954190870c5be6fd7173806ddfe16a3b97eaa9274ab3727f6be5d8b
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6f61d8cea27ea558e098aa37eeabb654da152e8191d8bdb035c98bd21680bc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272323237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa9468921dcf61b63dd9f32548a9c12bcc58af28f8e4904799dbd2788e85233`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:49:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:49:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:49:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:49:04 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:53:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:53:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:53:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777e2a7cd2f8867774abc2b31adaed051d2272be9ea6f534e24e079ece86647f`  
		Last Modified: Wed, 25 Feb 2026 01:50:37 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac9b8a27909288bb59d740df830595ceb4cb641e9a39f9bd8b7c03ce661601e`  
		Last Modified: Wed, 25 Feb 2026 01:54:54 GMT  
		Size: 87.0 MB (86987983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43864604b6884dd28827c49a08a7127c2f11ca53f03c1af3998d87c0fdf972`  
		Last Modified: Wed, 25 Feb 2026 01:54:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1bdaa1280a28d80ef03c0a508189c7f18c06642dd37f358930acab95e052fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7686446ec09f0ae1946040995cde299472825e315bd6af28d7ed3d902909ba4`

```dockerfile
```

-	Layers:
	-	`sha256:cb532b218fdee9531523c45f3e45670de4e1823af10a2d568b22395e8b97c6b7`  
		Last Modified: Wed, 25 Feb 2026 01:54:52 GMT  
		Size: 7.4 MB (7401531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae098efc4ab03254ca0c3a3b04d15b23f334e633b5c829d714b54f814a32e9`  
		Last Modified: Wed, 25 Feb 2026 01:54:51 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:35c84e000a3ce15596cb0b8d3300e3d3920aff5f24c47b1bf7abe18dee130129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253674454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1e7028e0e5ad4000b9e9cccfbcb46d0dcb36b6a0b0ef595e39cedf714bf53c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:11:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:11:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:11:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:11:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:11:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:14:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:14:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:14:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88825d23886aad7630f698fabec26ff327fb5cc56e608c0be4067ab5b8f57c4`  
		Last Modified: Tue, 24 Feb 2026 23:12:49 GMT  
		Size: 126.6 MB (126562035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161ad4869fa8a5d96e64255a6f2a61ca05d8e4efe8fe1523a5a3f192819e7cdc`  
		Last Modified: Tue, 24 Feb 2026 23:14:38 GMT  
		Size: 80.0 MB (79963689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1bba1e448acf54ab2c615a070bfffbf5f4572661322092331bd2dc0203ce7e`  
		Last Modified: Tue, 24 Feb 2026 23:14:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:679d7a7254b7150104566b05a7231a3a087ce7f4d5ec2c961225bc282f99c6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ea7eff0e0e29505297de22cfb04e2819c299c9a96b895141a3700de28e7632`

```dockerfile
```

-	Layers:
	-	`sha256:18f2fab9cd6124bb57b0f50c4cb91f17590f2395be585a1c555947625db8b0d8`  
		Last Modified: Tue, 24 Feb 2026 23:14:36 GMT  
		Size: 7.4 MB (7388253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c43600cb988e0d3bd0a45623008bba8b76f881476e99f770b5350e05b23e7f`  
		Last Modified: Tue, 24 Feb 2026 23:14:36 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
