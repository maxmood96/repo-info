## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6046d4468d0e498b34bfaa4a10e011f70ea6ab47c6e7d0e8630ab6bfd05df102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:607375a1d63f325e8157138bfe674712b1b22bb502aa1ecb9a8cb66f07cf9584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178495096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45e5f938264b7eee906a98c86f06ccd210a37cd4f7f9bf3339e90674497d21a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:52:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:56 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2f5b8f72f6dd0df20d5e49e6cb478188753630a3798d922335989ee1f33a63`  
		Last Modified: Tue, 24 Feb 2026 19:53:34 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d35bbdd29a9f7758f5255f02839def506059245d33dacfe20f0101de2c3a0a`  
		Last Modified: Tue, 24 Feb 2026 19:53:29 GMT  
		Size: 69.6 MB (69567948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c9df5204bfe9038c424f860e30dc4417a57497cf54a33263339b8344df95cc`  
		Last Modified: Tue, 24 Feb 2026 19:53:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28231b5549b7832f1c3d610ed02ab602076eda9d166c91366c0a2534ba8287d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad621b0167c64db20facab3afbdec0435f8dc217bde7e594d27e130606fc22c`

```dockerfile
```

-	Layers:
	-	`sha256:daa1fe90bbcc421773856eb2bbbd74c2fa67d1ea40d1e72becb7a7d8f076b684`  
		Last Modified: Tue, 24 Feb 2026 19:53:27 GMT  
		Size: 7.5 MB (7528751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f52c0880566fca0f077ea95b0896bb06a3b5fc2339feea096e63d8cda7189e1`  
		Last Modified: Tue, 24 Feb 2026 19:53:26 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb88e348c80a2dfa7020415fd370043c49b7d75e9e95d4cc3d5074c5fe4e8acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175f46a23d264e99c483ee303e862f9212944591a764a3c4627a548075cfbcd0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:02:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c00432273b608ee5a2ed0b29a44e0b0ea71c74c3fa9b3e3e6ab11ce982610`  
		Last Modified: Tue, 24 Feb 2026 20:03:15 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f1973cfc0e97c05869efd6d04c8a9d0d4e3577fe25d8a0ad4e4c7ea7e1074`  
		Last Modified: Tue, 24 Feb 2026 20:04:01 GMT  
		Size: 69.7 MB (69708828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4418283812d56c80510ac6a2e3d3c8032558cfecabfaf18b5abd0298ec0444`  
		Last Modified: Tue, 24 Feb 2026 20:03:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae180d03879eac5dca6cbed43c98d0762aa097e6085051903b074b807258396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f672d5bee59d2b31d5529b0a1059b77af95270fe0ad4c207e77b6cf900e6ba2`

```dockerfile
```

-	Layers:
	-	`sha256:01dabc6893c5657fd64b21067ab3167a07b594bd0a3fc5f753d2be951e19c4d8`  
		Last Modified: Tue, 24 Feb 2026 20:03:59 GMT  
		Size: 7.5 MB (7534550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099d8f718fdf2e399220612f8ddc7bf6dc7aab6ca9b534dff0e42996a4936e99`  
		Last Modified: Tue, 24 Feb 2026 20:03:59 GMT  
		Size: 13.5 KB (13512 bytes)  
		MIME: application/vnd.in-toto+json
