## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:4dc981928723e6c456fe416af78d5cb370ec10ff3964c04c090c580db357b00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03e605a471b447fb0cc319b34f66ab7e363e010a55f5966087af8e6ba090e154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235793742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94cbe90c8562a0b9e3f840a66b97106b016625e254fcca7b004dacf31e56e8c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0f1f137ea0ef5feb9c5819dd9c391408efb151f5acf0107ce7f648e855ac11`  
		Last Modified: Tue, 12 Nov 2024 02:23:53 GMT  
		Size: 145.6 MB (145601317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a722cbe8b0e5596c8020bf7d2761b5d9d5a2cdca4051392ed6d47a21d751ea5`  
		Last Modified: Tue, 12 Nov 2024 02:23:51 GMT  
		Size: 58.7 MB (58740221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03350173f756c2aa27efc02cde05cb6c9905e8679125167b4cb70894c888effe`  
		Last Modified: Tue, 12 Nov 2024 02:23:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e2da9c480c4fe0af4a1cd2bd13eca5ca6bb7bb188aa3635443283084f74af6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383caa2e375dbef2bd94ec610123871e7f9a7992ea120c8a0f08c20e4b5ba117`

```dockerfile
```

-	Layers:
	-	`sha256:53d8e77f049531ee1f87683bd672602908e9f4cf1a9b84bce5617e92199a8fa0`  
		Last Modified: Tue, 12 Nov 2024 02:23:51 GMT  
		Size: 5.1 MB (5145523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f610198af06a4f2c27d22008df15fa16b3000431e1611972cf6024b16e8a2c`  
		Last Modified: Tue, 12 Nov 2024 02:23:50 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87b31c50f59d3179b2ff1ec3a371691c1942f28bd443b11cea249207d55c86d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231359297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7254a9c8ed66a267dafe32e5e064cfb500781032bbb0a7cf7f8f3232c404bf2c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdddab0b8d7957c490f2c3727a8e258d7fb89f57866fed553019c199cf524e8b`  
		Last Modified: Wed, 13 Nov 2024 01:16:17 GMT  
		Size: 58.9 MB (58877962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed40685bfb9ffde5d06ca7fb6fc04c7338be0dc5811a502398b8f14a03fdef`  
		Last Modified: Wed, 13 Nov 2024 01:16:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2114507a5dd4760f48bfdf33c66a2020813eb88be4c2b4f06bb1611c3fa44ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e31ebbec484c36378fdb3e76a0c7adb62df65d09afe842b81b98151a0fe68b1`

```dockerfile
```

-	Layers:
	-	`sha256:02e99d4220e8dac7d7550ed0cced43ed937bdcc230d639e07b52f532b7a6d48d`  
		Last Modified: Wed, 13 Nov 2024 01:16:16 GMT  
		Size: 5.2 MB (5151879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52fee52f9af7ec596700ecdb10cd986727684b4448488f02af0da3078f1a61a`  
		Last Modified: Wed, 13 Nov 2024 01:16:15 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
