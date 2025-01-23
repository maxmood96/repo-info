## `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:a1f199b375914c5841363e2ae99d1732d15b91a9ac087f23dde1aa51b6541706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8dee0489b2a3c24308cebfd21928f59ab59b690adc600f181758ef8769af4af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243341117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7f5f01487f58a1beacd9f7ac87058763a244229f1e8a4b87d205df2c5993a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905b1c3da988c994ef048fdfd571442bb0b1e16dfe9656f29ac0cdb3a9aa70e1`  
		Last Modified: Wed, 22 Jan 2025 19:42:21 GMT  
		Size: 145.6 MB (145601449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be5288df7a2b0eadf53218138b06b31dd8b80c02d005d1dcb7ae2da2b3de676`  
		Last Modified: Wed, 22 Jan 2025 19:42:25 GMT  
		Size: 69.5 MB (69526607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27714c032aedbe087d816ccce94ccc1d0688432e91a4db687cbff08de0b4e8`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2af3721e6bbb54856615e0c481555ca651129903d0fb00b056656d5a598a8787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f296c832f4489f7d4cf2afa1bf068956a4a0403fc69fb03551997d1503dbf426`

```dockerfile
```

-	Layers:
	-	`sha256:c190653ac373abcf1ce7dee0d4a1064743e547c357bfa380827a2f09a180c7ae`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0478d80567038fea1e57d40568f64f7b660df08d57c0d86a384f4ba568205000`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd7bb1064c0c5d524d991c10f4e46bb52f75adda965644135cd10a0af19a3cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239805769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe0e343c6dd5e7435b4a7e90b0e9da41e3c60e1cd0bac0850f86ce77487709a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229927e0bbafdbde903dd88575e843117d316d1d8bcf9499da887ac21b6b14bb`  
		Last Modified: Thu, 23 Jan 2025 02:35:44 GMT  
		Size: 142.4 MB (142389489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3e859e1e234b7c2d0296e8642221569fac7a516542363b491dd3184190ffea`  
		Last Modified: Thu, 23 Jan 2025 02:40:29 GMT  
		Size: 69.4 MB (69374603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d532645075200b3ff1297cb62a3e1be0aada9038ad186d721a1d5468eace89b`  
		Last Modified: Thu, 23 Jan 2025 02:40:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba2871845b9d35b33cf7046dc3a6569742074429cff79b04453cbafa12b254ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d446970ea10fe25deb43483b0b0abeac1959aaef88ed6a2edc5afd086b8f1c04`

```dockerfile
```

-	Layers:
	-	`sha256:1de910e529af5868a8c5c11b7fc51430f3c26a65439e351c9789927f1182e207`  
		Last Modified: Thu, 23 Jan 2025 02:40:27 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19aaf52aeaaa72fac4155a72c4bda3ddc162430e200b4d98a391ca0e2b240bf0`  
		Last Modified: Thu, 23 Jan 2025 02:40:26 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
