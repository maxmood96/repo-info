## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:3a64c8f377dab83e61e21149be20b6ceabcd6887268b48d46d17dc87a45eeddb
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:daa99a48fc5c07c2e978c5134be0c6466e106571918183ca0afede2fab46067d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282766420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41544c15dd576f518cf10d46ede1bbc68b18f50d93cdd1385cf5a35d4c8a289b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6398070702252e417871eedfe23da0ecf789646bc57bb318255ee8633647a0`  
		Last Modified: Wed, 28 Jan 2026 18:04:58 GMT  
		Size: 145.0 MB (144966642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82de003334e97febab4363b42748b59b2c0ef6c9fbdcc5ca6b240922b5451c`  
		Last Modified: Wed, 28 Jan 2026 18:05:01 GMT  
		Size: 88.5 MB (88513513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2703d35edc8f616437356ae129afa733e4064380f1e8386d8f364a0cdbb63d`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d91ed77904019efe90a50213e109cce3e619f0ff931fe0b26c69f57780e2986d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31777a8bec286afa4f911127fa602f6c4556381c6efaed582d337ce4bfb59a61`

```dockerfile
```

-	Layers:
	-	`sha256:1a29e963b8010b1457d8fa207de4ad5cda8b3c50f383764c9cf29f41c86166c6`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 7.5 MB (7487967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6532c3ffd23348a800a7c7aed2ca61def6b3b8efb0ad25394ef76b0b5484ae1`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9881bee800503083dd67ce96831be796f54d40ddf7e5ac2b65a374e09c87c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280071226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace3168118bab37fecacf0523e40d06b396ea84d00eaa8b160bf4322dd4882fa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:03:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:28 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6818e89f50c7157618626525fcbd76d4b884158e71b789028982a52d1852ced`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 141.7 MB (141729907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfd9e654212d615f2a7d2e60c3b1077c2f4bfedf7062932df288ed16b38ca1`  
		Last Modified: Wed, 28 Jan 2026 18:04:15 GMT  
		Size: 88.7 MB (88692592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef476f0da3382e5c12098df613d380e964c9bed74c68312ec9492c3471446b8`  
		Last Modified: Wed, 28 Jan 2026 18:04:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f1effd8ac7ae1f283a64e538709e83faa5cce99934f812c47be1ff8646b6af62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7cb9ecea6905057c12615d9fb9927c638155aeae7db8c499e27825882a84e7`

```dockerfile
```

-	Layers:
	-	`sha256:251e7a2141fd6ba87af1d578aca24000585f80b13e555ed4513c745c61f95f7c`  
		Last Modified: Wed, 28 Jan 2026 18:04:07 GMT  
		Size: 7.5 MB (7495615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9e3dc7ba0c0079a4f0e0cdbaf3ea0d815170b6e6d561e896b15d04ae8e60a8`  
		Last Modified: Wed, 28 Jan 2026 18:04:07 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae431fc64cc3dcc7572b9d32373ba748b6a4df7fd7b3bbf54ee349dec6094783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279340092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb904712a3333e37c6e49ea9a32d546954160ffaad2bc37f5138a230bd25c7e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:20:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:20:22 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:21:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:21:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50438e71707d989ddaa5d0fb396447216e15c2ae0f9452eeec43515a9f6530f6`  
		Last Modified: Wed, 28 Jan 2026 18:21:51 GMT  
		Size: 132.1 MB (132079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200bb210b9acdbab268c1290ebeb76c906d10d29461ec5bbbf5b8bf2f3d489c6`  
		Last Modified: Wed, 28 Jan 2026 18:21:50 GMT  
		Size: 94.2 MB (94152699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf2277115d14d1c373e2f5c941d939c637febaa76f035162fd524ff4689e4fa`  
		Last Modified: Wed, 28 Jan 2026 18:21:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f27de240d25b0145e83104d02f768e01156b526eaceced473cf692daec4f9576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8512ed1508d8c923adba115169e32822cb9da6802e3dc0f24c2edbafd6308a86`

```dockerfile
```

-	Layers:
	-	`sha256:01d49ed29b065ef542e9a8b73d9ba0ee29a9c02d44a2719381dbc3e90753b44c`  
		Last Modified: Wed, 28 Jan 2026 18:21:47 GMT  
		Size: 7.5 MB (7491773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1893a81d6045453b56cbe84ada671ed60874615ab041b09128cdde013d32aa`  
		Last Modified: Wed, 28 Jan 2026 18:21:45 GMT  
		Size: 14.2 KB (14231 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cdd2dc1c590c16fa397fcc0c6933f8d31547e8d48be0e8e6014c2502a7b6d154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264175686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218e16a1b3d08eddf9a1d76fca7f977cbe07fdd1fad226acc2a05e80cd0af677`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:10:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:10:51 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aae73d6ca9c475bb213977dcd29121719a295968930d64b57e8491e3a1f0e1`  
		Last Modified: Thu, 15 Jan 2026 23:11:36 GMT  
		Size: 125.7 MB (125694843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aceccaaac67fc66259386e0802c8b450f355d1e724480b189045d4cb200cf93`  
		Last Modified: Wed, 28 Jan 2026 18:02:56 GMT  
		Size: 89.1 MB (89131495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c20c8a6c2ee7558672922e383505c48ec0e4d8d7409ee4cebac51954f1878`  
		Last Modified: Wed, 28 Jan 2026 18:02:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1619efcc1cd876aa271f9b3dcd159bb19db5837fdb0761e847dca171c069f655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffb081affe4ec54cb30650e5683169c359bd227e232af19db2ddcdc112c545d`

```dockerfile
```

-	Layers:
	-	`sha256:da6934351f91c17168c8385e38fde9751d3b0afeac043dd6f10aa858dc0edf7c`  
		Last Modified: Wed, 28 Jan 2026 18:02:55 GMT  
		Size: 7.5 MB (7483893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b8b5de8c1d0fc1b92dde6caeee348a2fe183800e27bd011e7f1163480181c3`  
		Last Modified: Wed, 28 Jan 2026 18:02:54 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
