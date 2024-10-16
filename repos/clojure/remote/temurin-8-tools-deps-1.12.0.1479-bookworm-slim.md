## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:b672a2c0f36ebea05afef3d63473e864f0087def1d53ffb33e79b583c45c4d22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dac0545600a10f316df3014ab2184a5601898019bc82036a4cf1ed2f34ed6443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a278c3ed21296f3645aab933724af1334a2faac3e71498e3c2f8d75281ccf7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9501221c4feeaae24fc2555013b626aafa4ad6b61ab37903536e2d3bee7d6b6`  
		Last Modified: Wed, 16 Oct 2024 16:12:47 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edfa11f0b789febe0c1798f127adff48e3ba11de291f1c8490d1305dd52272b`  
		Last Modified: Wed, 16 Oct 2024 16:12:50 GMT  
		Size: 69.5 MB (69482822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4764a3c272c633a12ab21ddf774a0561929d5d8346437a216d00bc9c3488ea`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de5ea8132ff5d342acc963ff91d5f4c3098aec8ca23ce9d2d1bca770dc4ca781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2751cb4a0415b42c3ba409cd6d29cb6045c1ebb32a27b06fb8688f865752603`

```dockerfile
```

-	Layers:
	-	`sha256:8a7522299aed74aa1991372236b1820e296c1021b48f9872c0f47f76019eb87e`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 5.0 MB (5017017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23953a7b7097766b630a6dbfe7b157c792105379d3077e1f179693f756de87d2`  
		Last Modified: Wed, 16 Oct 2024 16:12:49 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b67daf0919f4533c514be00c19785e407041d08e44be968c6797cee9d97efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf17cec65d100a4d8779b44da9d05811b8a01a415e2ae183354d890620f7d49c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0ff80dc6fa3adc0d8544c234677c658d2e59c27c7e75f64b0a08f60817f22`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 102.7 MB (102729219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d39fc7638acf3b0a9c52f74ccbe75bcc4b4fc25d761ae21c4ecd463b59777`  
		Last Modified: Sat, 12 Oct 2024 01:01:18 GMT  
		Size: 69.3 MB (69345394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb677580a0c9b1c00bd35063867450f403f55326422218f3f3cc21e5ef385d2e`  
		Last Modified: Sat, 12 Oct 2024 01:01:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e240d49cbbbe32955bd32cc45d3ff06c38e9683098ba3c08278e70444131e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449da0164e8a18d3ecaa09313bbc9d05d13967d78d7084379a5c99445df42eda`

```dockerfile
```

-	Layers:
	-	`sha256:e83654abe5be14517e5339272e342bf1c3101c19413113d7cbc61571ecaed5de`  
		Last Modified: Wed, 16 Oct 2024 02:08:17 GMT  
		Size: 5.0 MB (5023482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2178e04723e467c75f5d1b57c44def0aa76e3dfe2526b17d4de547ad01341dc8`  
		Last Modified: Wed, 16 Oct 2024 02:08:17 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json
