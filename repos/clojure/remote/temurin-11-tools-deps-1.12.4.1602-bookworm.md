## `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:5e1fb9fc5a42ef64a8676369a9209e7d1fcb88a30e6ab5929cdbd4566023ad92
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
$ docker pull clojure@sha256:1d410496a1a26da5381af43b33332c30a894c699d1f6de12215b50faee47f696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275438924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2abe4d9a0f6fde5ae467ff3b629744cd3e74fc028657a04c10918302bb4cff2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:41:58 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1c0820934a55f0e1bf8c32152dcf76b82017b72046623f466d00c4b53729da`  
		Last Modified: Tue, 17 Feb 2026 21:42:39 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042f3b7824ae71a5d32e16adea9ae4e4d7e920205254ab6389f59b06a433a71`  
		Last Modified: Tue, 17 Feb 2026 21:42:38 GMT  
		Size: 81.2 MB (81150039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8118a765e4f7d16c80100f1774c915d17cd18d1c41127b479104ca2b1f941a3f`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c77ba9f19ab1257460bcfb1d960e7944a2fc16e3226104522b22cf18ddb2a1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5555c62690ca696ada21c2caad3388743e820c2c3f48e3b39631a3a04f77a77b`

```dockerfile
```

-	Layers:
	-	`sha256:73ff31abee6c2a9759e05d5de61b4d31869d8d201ba3594f51f82ed5556f75a7`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 7.4 MB (7396930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645110b048f8a32b95f5cb691d8db72960719eef7f5a2ef2bcdf1b9d4e95e834`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc05df0111002667ae9bc0835ba9104e22864689c15897637813feb5419647c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272006508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff95a34214ab7a7e7fece21307f8bb1b401ca5af26cb84510c51ca9c62748d68`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:41:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:41:46 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b248883a01edcfc8dc0cf9643511d1254cdf4f6564bba64f09f014c22ba401e`  
		Last Modified: Tue, 17 Feb 2026 21:42:26 GMT  
		Size: 142.5 MB (142501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bb3cbb8c015086c269e3003ed76b226825c320e0a676d9a09737b02f9e0210`  
		Last Modified: Tue, 17 Feb 2026 21:42:25 GMT  
		Size: 81.1 MB (81138483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4449c6a1714b57fe18d9668204224fcadecda47a630ee628b9b6bd2c998544`  
		Last Modified: Tue, 17 Feb 2026 21:42:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:279c41902a196313738e10ef10820038eb1680b92d72193c4802a35e5f7a75ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d860401ce8f4ae75a8ebc486162aab7a3aea01d1ef6222f0a1b5dfa8ad2f16d`

```dockerfile
```

-	Layers:
	-	`sha256:56e40fbecba4a46a2cfc900d825fde3b4eb6bdfdc0bdc87063f56e22babdd745`  
		Last Modified: Tue, 17 Feb 2026 21:42:22 GMT  
		Size: 7.4 MB (7403311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e7a2aa33cf9bf7fade2eb053964698ea35074ce6b79458d62e9045d377d980`  
		Last Modified: Tue, 17 Feb 2026 21:42:22 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - linux; s390x

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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

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
