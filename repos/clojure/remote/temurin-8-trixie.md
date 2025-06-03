## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:3628e792c7484aa8675d479539465dbc87d4faae79b6c1a3ea09ace1843c81b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c8e1abcf0d937f464d66998f502b9dd110c28a7207c6aff523c2d7c92e68cdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192171273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13771723792f9e91a2e95c68848e9337c8db8351b2ef10fe0a6542a30d5d05e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43508fe17b2b8209e262d3d9018ae2a3fd15aeba4e9d817bb685360657eb3072`  
		Last Modified: Tue, 03 Jun 2025 18:24:38 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31700e545c197bb3979d9d814a6abd000649ed171d074dcd11fed126e9045e07`  
		Last Modified: Tue, 03 Jun 2025 18:24:41 GMT  
		Size: 88.2 MB (88207540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002458144577738381142c7141d66e7ad9cef26c9c57533cbb27f1638d9520e2`  
		Last Modified: Tue, 03 Jun 2025 18:24:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2d0203b0b51e587acac40779602b549a45cb3840048002a4fcae516b40ce0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7454239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892674d3932753bebaae42a6071073cc41bbbfe213ee642eb83b9ca5ee6884bc`

```dockerfile
```

-	Layers:
	-	`sha256:7c632b75bb6440980ddb1da6d37a8c7ee5b67355b61beb85d65a16a90d9b1e38`  
		Last Modified: Tue, 03 Jun 2025 18:38:25 GMT  
		Size: 7.4 MB (7440026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37998ece941768fbba1f6076df4ec6286ea11d3018ef6ae55dbb1e65220cb287`  
		Last Modified: Tue, 03 Jun 2025 18:38:26 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5dd74b1e61830f00788f833d626b65c88540d60368dc16c81d13796d14f0cdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191960907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28250d960b7fdf3de0cdac7c888c5428eeec256f8ddf58d563f303558d0b8c46`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b438f9c0792eeeaa8637b24f8c401b4a12e19eef04c099112c78a727c9bf9`  
		Last Modified: Tue, 03 Jun 2025 19:21:35 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd29a9c6ba85f9dc89281e279caf294d3be11cab3af3ad1feef99d60a702d74d`  
		Last Modified: Tue, 03 Jun 2025 18:31:13 GMT  
		Size: 88.5 MB (88511451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27048e8415b4375d61f0053bca23c63e935f6c266b91dee754b6af70521d238`  
		Last Modified: Tue, 03 Jun 2025 18:31:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9119979c9d1843add81c1ac94e8be6865dbbb613a67d57f90b613ab28268c726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900c6094f372787b347ea55e26740c8ff38858e87c555ff5f96fa3dc839bc33f`

```dockerfile
```

-	Layers:
	-	`sha256:4390410a10b1e52533ef157a1964abde2f932e24761bac452d49e42b7389b39b`  
		Last Modified: Tue, 03 Jun 2025 18:38:00 GMT  
		Size: 7.4 MB (7447754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77555cb7b85132d353a828a6faadf968de57afb10094718dc375339889ac3d87`  
		Last Modified: Tue, 03 Jun 2025 18:38:01 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5a79da5f7144bcf1467d1baf55e0820c08f06b54d504d7673c53649288117bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199199462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4872e2e326c33d01c4a9e281b067b38be43c1f81ebcdff081641c768fe0791`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975f5c873cd794ffce77448d785fd1ca79428164a5e8dde7131d18ee75ac676`  
		Last Modified: Tue, 03 Jun 2025 08:10:49 GMT  
		Size: 52.2 MB (52167951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887a3c3798d2186877f756e0938956dc68c85383e4180fa0987183d3c30a3af`  
		Last Modified: Tue, 03 Jun 2025 18:36:20 GMT  
		Size: 94.0 MB (93950322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda1ec7a28e4bd90bf7d5b4bd9c1abf4888da5717182012d3f8363bbb20b8fb1`  
		Last Modified: Tue, 03 Jun 2025 18:36:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b8e8180a3d00582c76e740f15050ba554ad4efbf15d15a3885409bef99822f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd0dfdacbf3de9ada7150dae46a2560f2b67ec659d7fbfaff74edae938b59a4`

```dockerfile
```

-	Layers:
	-	`sha256:dbde33118149f3a9bf2cd939c138f0083f7e05615f37f699b40f5de6b7c3b4dd`  
		Last Modified: Tue, 03 Jun 2025 21:45:10 GMT  
		Size: 7.4 MB (7445036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ceadf174f4b154000a6e0b6e85e6ce60d128198eab4c77ba4e1b32d09c8ddb8`  
		Last Modified: Tue, 03 Jun 2025 21:45:11 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
