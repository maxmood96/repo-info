## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:254034ae94ee85c45f02f5909370f935a1dd702ea75a47029be2751ce41beffd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:99a16eb6394ab0cbde7faf80a3b75f9889896a036653ebab54a465cb89e3ca31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498d755fe612e1313acaf97375c01e9cecea993e3f51c63c3f08b4fd45524f44`
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
	-	`sha256:070fb27b06add8af90f91be0831d34a86ae7526d00684e620f34db9eb5e1466a`  
		Last Modified: Wed, 16 Oct 2024 16:12:59 GMT  
		Size: 145.5 MB (145549907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3116f9a8731e6048e9ffb4a18050e13b6c84ece2f2d199eed9d6a6378e27056`  
		Last Modified: Wed, 16 Oct 2024 16:12:58 GMT  
		Size: 69.5 MB (69482840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e98af714fb49179a4a2ca4596be13380145cea4e80096872c644d001a835c8`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d566f812d6d0ce61584912aa9cd38b46643d77948244774cdd4d610a2fe6c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248e2a4e6ad190520206a3dba775044efae5a0dc37ad29ec5eee8296c5e01a96`

```dockerfile
```

-	Layers:
	-	`sha256:180d4822fa65f8c3fbb9d45c562159480c9b317e0040001d0b2400403af60c1b`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 4.9 MB (4915018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600b4c810fe193ea102ac944c1d12bdfbb5c262705b46d18082227452c7a4e0d`  
		Last Modified: Wed, 16 Oct 2024 16:12:58 GMT  
		Size: 13.9 KB (13946 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8e182beb4064be7a21c3f3e4efc2240bf9c99dee6e6a38e88263e618070ef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240858777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1c765c12c0c94e468a8b38e902d984849cd66fec3b784ba1bbb66fc09cb125`
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
	-	`sha256:7689c16b847a420d23f4ca2ffebc6ef4d5958859876ead4dc27352437cdac4c0`  
		Last Modified: Wed, 16 Oct 2024 02:12:38 GMT  
		Size: 142.4 MB (142356566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b411d27ed878126185944103c1568bc186b13a0fcd27fe101692ee41ecf16`  
		Last Modified: Wed, 16 Oct 2024 02:17:14 GMT  
		Size: 69.3 MB (69345194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cfe8c17dcfd4e7de060b306ba790880bd97ecea618efec0c7be09457a9ed99`  
		Last Modified: Wed, 16 Oct 2024 02:17:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8033b9e58bbbe1e4cb038f3b91d21b7baa46d90d5bc5379fc7a58545456499b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a38aceafcf6ecae7735e57f24ee55796221d865587ef8400d9c88296cd50038`

```dockerfile
```

-	Layers:
	-	`sha256:680e80385efe50f3137ee17a66a317d3f041225958a23f01d8620c8a334ed4e6`  
		Last Modified: Wed, 16 Oct 2024 02:17:12 GMT  
		Size: 4.9 MB (4921403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5491a34a5ad99e21a0adcaa42aeed3da3366c421b80d1e24e0dd6fc4eb1a11b7`  
		Last Modified: Wed, 16 Oct 2024 02:17:12 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json
