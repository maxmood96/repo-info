## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:b38007f183061684da5134484e039f7bf03d52c2565c006be70e1d9602d0bf25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:69ef5f1a0739a7e4197604d63c2a192755dd27c5228f497c88c627d2b76a944a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201158841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914fe90ddba3949dddc5feb4b5fa244ff9f6d4904fe109e4ca5b5fa197ef23d1`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084655cc98a606dba8a093db522b9db42ea92f19c7ee0e22a32ae15698c3f77`  
		Last Modified: Tue, 03 Dec 2024 03:19:15 GMT  
		Size: 103.6 MB (103633935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5681a11def878778e6d3934a5bbb83a743045e48cef01b8d09a10fe12a4b306`  
		Last Modified: Tue, 03 Dec 2024 03:19:15 GMT  
		Size: 69.3 MB (69292682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d201248ed00c0e909fc585153c4fb455ddddcd80d3a14aea919febe83ea26fad`  
		Last Modified: Tue, 03 Dec 2024 03:19:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3c07fd8d271098cd5e817eb78f4b66d790fc5f664fd17d8b82dcdfd654f2f5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3e435a543a0f1caf83e06b91ad5062f6b65a0315c4cbc1aa9b8e8dd69f76cd`

```dockerfile
```

-	Layers:
	-	`sha256:898a6cdc1374d8dbe3932b890a7181eaabbbde01c9a012d2d92cdda4c0fe340b`  
		Last Modified: Tue, 03 Dec 2024 03:19:14 GMT  
		Size: 5.0 MB (5041550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4c72f28514a631d6b9c2032bf3fd118ac893d434f03134967614fc46032d74`  
		Last Modified: Tue, 03 Dec 2024 03:19:14 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:552453709959ba4b1beac255eb4089c60f9b8609af001a49e7c6dd6103fe727f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201240805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bfa528b5c478f891ed1d64aefe88c47535fe3ac6582d89bd83fd325eea7861`
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81788011a7c72bb7b64e7d7ba06b654cf3c457826b14241b9a03dbd607de9f9`  
		Last Modified: Sat, 16 Nov 2024 05:12:00 GMT  
		Size: 102.7 MB (102747711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b419e87441f8d944faa75e3c807dc0f84eb46581c5ad7e50e52491c0f4cda0`  
		Last Modified: Sat, 16 Nov 2024 05:16:37 GMT  
		Size: 69.3 MB (69335094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352425d366459baad27542ce17f5e141571c8d1dd8e6e99ae837af434ed37785`  
		Last Modified: Sat, 16 Nov 2024 05:16:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ab5f44f7cf3326dc163809d77178c4187fe20da8624d86500cbaee14b4a85aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c635619d2cec993461ea4838f5c9eabbd51c050499c9bb5a998cc48aeeb5715c`

```dockerfile
```

-	Layers:
	-	`sha256:5bdec757eb744b88757c0f8db0e271d749e4cb7974a4d245a1d87ad50f732e4e`  
		Last Modified: Sat, 16 Nov 2024 05:16:35 GMT  
		Size: 5.0 MB (5049263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66cc970076e76b4520d3793c1164f47bc31c1be8ae8bc7e8d5e0f21e51c9693c`  
		Last Modified: Sat, 16 Nov 2024 05:16:34 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
