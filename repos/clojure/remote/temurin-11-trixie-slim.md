## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:573ae846dde2fc73cf47f0f55ffb082c990e480ad185e7d0c7653a791dcc58ac
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
$ docker pull clojure@sha256:4b37ebe35ce30891017e46f0b75ccbd4500f4aab1dbff753b5d69a1cba0b1313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249685699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350b01002403a76a7c03f16d5bda2a359302d27339b0e5217f5d358d79a89a1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:04:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:36 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310ffe5beb7bafcaf2aecee4d15531719860b18ae5f23ab7f4effd171479c6e2`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 145.0 MB (144966647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0255e3a2c2eb221a3f8c43c8229cd74c9335223bd57ef0a3da2872dfe57b0d2`  
		Last Modified: Wed, 28 Jan 2026 18:05:11 GMT  
		Size: 74.9 MB (74944721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76bad87bfd06c69d92ba3538dbf464a7422281479dcc8eed4c44e47efe48a36`  
		Last Modified: Wed, 28 Jan 2026 18:05:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2a28ff793db23cd0769e8b563f3777b790a1bfaa9cfb3d3c263681e079a9c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec2cf30b8d60192669ff7551653b3d9209333c6c8c437c7e9382f677ae477e2`

```dockerfile
```

-	Layers:
	-	`sha256:dc73cb549d29e5dafc83ce77e88b60ccb45133b569143f61837a37917f3634d3`  
		Last Modified: Wed, 28 Jan 2026 18:05:08 GMT  
		Size: 5.3 MB (5276438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8270706782d0f53c2d1f3a18cc4142bc021acfe6cd918cef45db1b9372eae6f`  
		Last Modified: Wed, 28 Jan 2026 18:05:08 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6691e5f78d8b7f0216b7870ca21b195f8577a1119efa60cbdf8ad971108d683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (246986979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309c91cbc0a289b389f163688370028a1d7d3c8590d5582d4bcb351992ab9499`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:02:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:35 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2ce72d78adae6ef325a9a9d6903c1dbdff4648c4df8afecccb763d77bac224`  
		Last Modified: Wed, 28 Jan 2026 18:03:16 GMT  
		Size: 141.7 MB (141729882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4226c798224e4d50563639172a8b6f559db29042ecaa798a7251fc2e0953b03`  
		Last Modified: Wed, 28 Jan 2026 18:03:15 GMT  
		Size: 75.1 MB (75122410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2907441fc020b2e9b789bafb79819dcc279151627f587a432cc478602890ff`  
		Last Modified: Wed, 28 Jan 2026 18:03:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25b6fdb73f8b2a1dcf6ee940bb56cdc3fa382393d6f8bf960603b1d5071ad398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22827dbc89ccbe86dfda4ea2688a3cbcc12c4a5113c7ff219a510cc678408c58`

```dockerfile
```

-	Layers:
	-	`sha256:29605fbdebb766edf13e7a3595ab750ac5dc410cc36ed193fbd28e8e1e565077`  
		Last Modified: Wed, 28 Jan 2026 18:03:12 GMT  
		Size: 5.3 MB (5282825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1dd17a2b1b7e08764519c6650a52e2b0170487b0d5b4cce8911483f2521727`  
		Last Modified: Wed, 28 Jan 2026 18:03:12 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:61f80da6714605c726a331f7f91cd3d9ca0ec869ab0021af54c8585a9a20b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246266945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8ba21b6e8f5738f33d56c06a6b441d5a31edea711669a79ac21a29e0a1b99`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:21:26 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad69adfcc4d51808f6f22619ad46da87bc82e1dd7a4c8618619435d6ed0b7a1`  
		Last Modified: Wed, 28 Jan 2026 18:22:50 GMT  
		Size: 132.1 MB (132079784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62f3e30f747c9deca0e68467873cbf71e6f7bf6760948e3c8b35917ec25672`  
		Last Modified: Wed, 28 Jan 2026 18:22:49 GMT  
		Size: 80.6 MB (80590916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023d64163d453483621baee1e0865fc486aa1c5cc553b9ffb260976f1f64eca`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a167b5fce33f48dab35bc5f434b22340a21493dc2ad3e201be36a5698c5027fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2baae8c0a396bb9d89594470cf9af03874bb3ee922299eb58e2c11294b3c35`

```dockerfile
```

-	Layers:
	-	`sha256:1408b2dd0acd58f3cfb51ee16bada4dadabb0c01394f1338d923509d6c8804bb`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 5.3 MB (5280194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5326df07dad645d3350e9083ca38ba0745ce2f00ba915ef955f129482155c8cb`  
		Last Modified: Wed, 28 Jan 2026 18:22:46 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4beebb72e561409c3978b092b268cbef0ce38cea4d87c26fdf19935e52eaefb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231096014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5eb14c15a42817da23c2b8903e4ee6ca5bbf517db3d6837134e2d1c49738c82`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:02:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:01 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bebcab3acbc63c10c106b89f5b32bb956ab9d528bacc0e2ff5c372a77d9fd56`  
		Last Modified: Wed, 28 Jan 2026 18:02:53 GMT  
		Size: 125.7 MB (125694863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f897b7e37acb96f2ec7ec359b465022aa318c8db8f3210449e6d8e5b43fcb`  
		Last Modified: Wed, 28 Jan 2026 18:02:52 GMT  
		Size: 75.6 MB (75567095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0c14da8e6c79005b57f40fb00ed6dee88b3f9f01e754eff9a90ed7202dfc2`  
		Last Modified: Wed, 28 Jan 2026 18:02:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:653e320672a07822eb235aff41334395ec8be3592ea6e502bc473b4452ce5ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b1ddae824fc3ebf8a27327d0a0a0f193acb36265b2a719ef89fdfd39283955`

```dockerfile
```

-	Layers:
	-	`sha256:2753df0b87cbb941c0fa3a229503f48106c5cfb6bb2dc3e1f1f40568e5e655ce`  
		Last Modified: Wed, 28 Jan 2026 18:02:50 GMT  
		Size: 5.3 MB (5272366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8f6fb13718e0d2e607b007863a77848d1103bce9b1c100444787876f22d4bd`  
		Last Modified: Wed, 28 Jan 2026 18:02:49 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
