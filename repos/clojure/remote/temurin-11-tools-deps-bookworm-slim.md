## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b302aa470d40e28d8a3638907d29aef645b8f93d507d43eb54d86ecce6a14231
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bbafbdca660ecae2ed8c5e2a3e7c076da9534a777680fd9de610aa47cbcce5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48649c1634ab55519cfeea466bbd77d30f732359f120ccc5e76638577dca5c5`
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
	-	`sha256:d12a7fdce1a8364c12b8da62752adb77ef41c13c3968078d496ef6f86752f432`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 145.5 MB (145549934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb74e7583034eff440d8d7d5c8a64e6925304256476a0f340899d0f75cd750`  
		Last Modified: Sat, 12 Oct 2024 00:53:52 GMT  
		Size: 69.5 MB (69482703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c625ce6b53d41db71dae10d56731f3662529458319bdebec6aa86723b0a5b7cc`  
		Last Modified: Sat, 12 Oct 2024 00:53:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f380f8044440cd68b32645eec843c562bc116ff75096a865d03b5b3fe4a9560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc35386af4a8058b527bb77fbef6558192ef979c721c0b4183857a20c08526a2`

```dockerfile
```

-	Layers:
	-	`sha256:9448b2b488902953b0aba6c1312692579d2db2873cb28ca8e8096b8d067e73d4`  
		Last Modified: Sat, 12 Oct 2024 00:53:50 GMT  
		Size: 4.9 MB (4915018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e68be670c2132e817bd9d3aa4806791a23347bb0b65fc00dd2174c881c5ab93`  
		Last Modified: Sat, 12 Oct 2024 00:53:50 GMT  
		Size: 13.9 KB (13946 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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
