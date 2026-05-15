## `clojure:temurin-8-tools-deps-1.12.5.1638-trixie`

```console
$ docker pull clojure@sha256:f779c9554ec670cc7fd65e3842b947157d930d9e83c4de8ad9f7a65e3747bfc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1ba9a45ed6ec63d87d1d47c1761a999270e421dfe69d70913747f54cb8e136af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190105519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9aef1fd67e13bfb87e59c00567edec62b941367994dcd833b9958986dececf5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:33:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48b4f9493d28a3a9a91eccbed6b9adff6146de1ffe1c8e63776cb918f8a44f`  
		Last Modified: Thu, 14 May 2026 23:34:25 GMT  
		Size: 55.2 MB (55198702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34981467fa45df29dacc816fe3aebe159f0f2b81e0b4ba92274128ae7b8372ae`  
		Last Modified: Thu, 14 May 2026 23:34:26 GMT  
		Size: 85.6 MB (85603850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8172757b9a8f02d32bf2845af6cfda609da07a9fff637b3b9da72c46a0d251f`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7dfce1d1214bdf8d4f1faae73fff39063c3e122d427f93d769a0d93b3ff5b790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552b02ed9c10778d6923918f4da123561d61e9a446c42349a3f0010b16a83c7f`

```dockerfile
```

-	Layers:
	-	`sha256:9505372f08b3f5873b955b145ebf2b239550add6cbc2365d3451a1d6dfa128b0`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 7.6 MB (7591742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a2e875d9f3c795ded8f8d80b6ce5fc8d901468843ed6939ede554807006071`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99f1f25db6d1fd792c61e7c973dda0a4341a7021dde86940fef1e873471d985a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189358259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46f05605460db4aca5f4930bce15ae210e6b143fe72a557551eae8ba551309b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:04 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:04 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1667a88d4c722e369300e6ab68962fadb83f736bfd6c51a1949a1a11af76e0f9`  
		Last Modified: Thu, 14 May 2026 23:34:42 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a177f37ded81606323046d82a12b89dad46fe9bad7c0a1d8cfceb428a393b3f`  
		Last Modified: Thu, 14 May 2026 23:34:43 GMT  
		Size: 85.4 MB (85415246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90fc3ceca744f000a6bbe4cecff2f661a8cb9b55b6fa339fa5b866e5bbb0873`  
		Last Modified: Thu, 14 May 2026 23:34:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a337b890acc1e700fa76239824f265afc162fd5a8c57885c03f48a8b6a587abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72d2d879d74a9fe02348e2fe7b5e64b88a10b17de88f91a116c83d40779249a`

```dockerfile
```

-	Layers:
	-	`sha256:215a44c3e9d4b4540218f797a0596caab295653ffe30f579e6d2f6a99a8cdefe`  
		Last Modified: Thu, 14 May 2026 23:34:40 GMT  
		Size: 7.6 MB (7599472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993a59dae25126bf606cf1aedd159494cd94e4904201ca77e3fad98edbac92dd`  
		Last Modified: Thu, 14 May 2026 23:34:39 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c584092878940715448a384f4eec74b86d2ec6614db879aedfa3f18df92159a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196801223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3529c8162a4f98166b45ce5ebc0ac24ed31bdbd42910731972a475a29dcdf3c2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e12c921f3a94005ee98f78639eda3708949c3e17ae8fa1f27ee8fd891b707d`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 91.0 MB (91008260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93e9f5f24ca206805bd7f24fb27f0aa84d313b591be5e45ba9b622806ddbaf4`  
		Last Modified: Thu, 14 May 2026 23:37:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e87406478a553bd0bdf848a1aec259aa2194380e9e928b92a4dda85fcaf725c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c464af8b8d028639079a8a9337058cde2368165edac24b383bfd585d991b78a0`

```dockerfile
```

-	Layers:
	-	`sha256:84de900e654d7dff6e612caa97f654b509ed04df00702489aa318a74b6bdefb5`  
		Last Modified: Thu, 14 May 2026 23:37:04 GMT  
		Size: 7.6 MB (7596758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f81daee33c6acf61dc0ed5fb4d5083d126757c050be480191a68609e7440ad5`  
		Last Modified: Thu, 14 May 2026 23:37:04 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json
