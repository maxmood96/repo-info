## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:94b85eb96cbb55ac876e283d81a33f97980f71f94bf191876c51f14d0a5f682e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b31007b6d9bb3fed1ac47824e926a50f8f4e3f835fdb825b7a79fcd2467e6caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199947371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6fbd5a7605ae8ccc0b99b4b3acd4a15c6aa7c2f2029df7ec98f8b16b35a0f6`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195295c73134e395e2634b149103034a56fd81282c0c9b6d2cac4878f2477e54`  
		Last Modified: Tue, 03 Dec 2024 15:02:01 GMT  
		Size: 102.7 MB (102747754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222c126fc4983c6d7e0274e43de640f8015bad6a079d15caada44b926b2f1f5`  
		Last Modified: Tue, 03 Dec 2024 15:06:18 GMT  
		Size: 69.1 MB (69140161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4087ef9802834ccbf3f458e229ca75af9b7c5468f9d6cd780d2bd83363e0ac2`  
		Last Modified: Tue, 03 Dec 2024 15:06:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2215c7730f92f28410f063b1a41e80285c993b67c380fcf6137c0e146e34177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5062429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ecfa7627f7ffd0a8663d24ea84e5eaf2da2da8e424af97d0d81866485c8024`

```dockerfile
```

-	Layers:
	-	`sha256:425b2379c2a449eba18c26887efea54e52e2ee449c4dfd2ee10a51d7e02e09fe`  
		Last Modified: Tue, 03 Dec 2024 15:06:17 GMT  
		Size: 5.0 MB (5048015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47409e3745c81518bd60f4b22964c79e875b21c1bf2ea5b468c807973439ba2`  
		Last Modified: Tue, 03 Dec 2024 15:06:16 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
