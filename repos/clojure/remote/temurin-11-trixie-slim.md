## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:41dc670dcf588ebde9ba7a0746ee389431fb3492cc990744caf2a42b573e98bd
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7bd751cff22e6a6c393a13f034cf3ae6b74a06355656a11d4160f1e108c617be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247678165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec23da3f51e384abd0e65b2c2e47fae9faaccf159e92a93ecd37612f428b8528`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:07:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:07:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57fc64de21529cd21cac23dea0640a7d917d5d97f2bff4b7ef508abe6ca5be`  
		Last Modified: Fri, 08 May 2026 00:07:34 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9698048c4a90811286d7a881983a840f8fb7c70627ba7f55866205b5ba47bb4`  
		Last Modified: Fri, 08 May 2026 00:07:33 GMT  
		Size: 72.0 MB (72011153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d924c5c29e899ac5e353935a4dacbb841ca83148566cc078329e77cf7ea19332`  
		Last Modified: Fri, 08 May 2026 00:07:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec0b70fb919348e819ac426c7bde2bb971aa3a87dd8469e3a5d6dfd21a6da934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183fead75f6d21d23a9d1ceff438b00fddd9e14367025cd838da70a5a9011fba`

```dockerfile
```

-	Layers:
	-	`sha256:87f5e3d75515f4916b158eba5967731d5cf456e73a3a67cfae89f5ed9f924257`  
		Last Modified: Fri, 08 May 2026 00:07:31 GMT  
		Size: 5.3 MB (5279335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f393c5c80a512e7299738ad1a7be75180482d18f396759c38ab486e1650a92b2`  
		Last Modified: Fri, 08 May 2026 00:07:30 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:069eafab19ae11bc30fda73702a01a3f59763aa360d6dd8e8342f5134ebfd3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244557760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7e344d70ad4ae382a90e4c6fbc2f75adf984f8c760d02d8944cd5fdbdf2c57`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2b472999165028200a3763e277d5915819d29f4cc156a7db994c22c536d04`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1fc771f7579cc14570e0e0991a46aa00d99811e7244777bbb343ca44c0a69`  
		Last Modified: Fri, 08 May 2026 00:09:08 GMT  
		Size: 71.8 MB (71831275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f582307c1355a52702ad5c5a1e7d48e8aad096f35f0a48467a77402aa8ac5`  
		Last Modified: Fri, 08 May 2026 00:09:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:351684b72cbd48d6a0481658ea8d11970459e8ea88c9779bdb8e885438b97bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dd6f71b38f58a24bfb24a0bd37ec05f2e8a84524feae22f42a890efe0edc81`

```dockerfile
```

-	Layers:
	-	`sha256:84569782a0bca256a581a81dde716d953fc8eb10bf51026b18eb8887b43629a5`  
		Last Modified: Fri, 08 May 2026 00:09:05 GMT  
		Size: 5.3 MB (5285722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2184d2a254c00f60f6cf091d6506636ea892e1ddbbbfaaf8f2edbd22cb27f32`  
		Last Modified: Fri, 08 May 2026 00:09:04 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d12b4a917b73955c3be2f1f82de114c5f75051e773b8324fa5513a8638da6adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244137549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a778a4ddc2842b9ee863412de0c34eec1a731a9b5d66b65a39bb632b31e0356`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:59:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:59:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:59:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd298a1e1654753929706776995581c6d8e0ae8db97ccd3dd0cbc779069c0bd6`  
		Last Modified: Fri, 08 May 2026 00:40:09 GMT  
		Size: 133.1 MB (133110194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edea885d9a8c96b6a82ea83d56c6fe4230b0913e895fe906ccc14e51ecdd0651`  
		Last Modified: Fri, 08 May 2026 01:00:19 GMT  
		Size: 77.4 MB (77428678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29c737a001bfd61b7b0adbaf89eda9fc605d6d4890639ae491280aba8c8c2a`  
		Last Modified: Fri, 08 May 2026 01:00:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e450b40f37717e6be3400076d1a4554b826b30096e5735292e401748c62fc401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71d6e415b5dc7c4e7868680d5c9878ed122800dab78546ba25c45fe995d80d6`

```dockerfile
```

-	Layers:
	-	`sha256:b1ff2cc0b72b82805e84dbb40077095cf53416e87f64f37ed4871059a3689e9f`  
		Last Modified: Fri, 08 May 2026 01:00:17 GMT  
		Size: 5.3 MB (5283091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b582ac8ca962c97912481fcac1429c1250f5269566121cb4d83e1c06e9ceaec`  
		Last Modified: Fri, 08 May 2026 01:00:16 GMT  
		Size: 14.4 KB (14445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6707d8089cc6f738d044b3e20609df92a5fb0f2eadbd7014de91770ebc3da9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229479264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7be4b030f67368fe3b66cc9b1605635eea93f75899f06a0035b0c1ba705a9c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:00 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd225ad1c643079b30473dae02495ff9d2b5d14eb066314672d33b5b2a32892`  
		Last Modified: Fri, 08 May 2026 00:27:45 GMT  
		Size: 126.7 MB (126651711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b11884e9bb8fa555e285763eb4c108612f7caf52f6275c92a4a9cafc20fb79`  
		Last Modified: Fri, 08 May 2026 00:28:50 GMT  
		Size: 73.0 MB (72986608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b51c35363df7df9749e18e8be8e5de3102c55a642389ddc3c03139d93e8aee`  
		Last Modified: Fri, 08 May 2026 00:28:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02dcd71b22d39885e30fee61af9346771683255fcf87a497cf6e4353d6d0aea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d3f4985f2c994e3eeaeb0ef0aa489d941df4a3b2eec19b3506de198ce5cd10`

```dockerfile
```

-	Layers:
	-	`sha256:15f57678392c59d4182d56217ec1f6dad6bb84e3566653f0a160b98709912e56`  
		Last Modified: Fri, 08 May 2026 00:28:48 GMT  
		Size: 5.3 MB (5275263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fc16e03ed46979370a210fa3fe80c3b4644a5524d89b8045dd28eb654eb431`  
		Last Modified: Fri, 08 May 2026 00:28:48 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
