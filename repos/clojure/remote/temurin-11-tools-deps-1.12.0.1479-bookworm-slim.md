## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:0c410dd739370c136355bfe067aa14f1f18a9b3c68a8e29e3157b0f6d091b0af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46bc3012c75fb4ce67d89a2600e5c3107726ca5a089b6d2ac2d35f15ca8502b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240857348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e81f6023e071ed68e309c399ef62e4ddc6092f35bfeaecb5dbe3e055a113e`
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
	-	`sha256:3c2f2e8461bb379350af396478be5ad496868e75a130b7e6dbbebdcbb87e844d`  
		Last Modified: Sat, 12 Oct 2024 01:05:51 GMT  
		Size: 142.4 MB (142355002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e9c746501f2c17b243d8da3f5d4e9249d1740695c7ea8198cb8ab01ca22986`  
		Last Modified: Sat, 12 Oct 2024 01:10:16 GMT  
		Size: 69.3 MB (69345332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9491a4dd3685456f7df6442a7af5a2092a2dd0d84976f601b79b99fccc669882`  
		Last Modified: Sat, 12 Oct 2024 01:10:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ea52b885ce3f9dd893802a8f01f5ca50604b94d1793dac82e9005fc4e311179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce777916f58c23d49f31e545fe59bb721464812cc5b77a47528e21e95cc393`

```dockerfile
```

-	Layers:
	-	`sha256:054b4c135dfd9ca4a1c2fcbe0f5172af9d5171f6b2cb7af9865e91a69a66428f`  
		Last Modified: Sat, 12 Oct 2024 01:10:15 GMT  
		Size: 4.9 MB (4921403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8159fadd1acbeef74358f9f056e6000436e3633af0e0171b5c088660941f841`  
		Last Modified: Sat, 12 Oct 2024 01:10:14 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json
