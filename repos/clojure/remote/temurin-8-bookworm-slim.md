## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:4f7cded3a4658e67460dc2c416e68d22537ec788ec7a8da6ba9599c790a74926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2fa994f615bc0ad4216bacb9ac7e4e1af8c79c4f4649167d2898c4878b19f7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d0c6d8463b8ef097ed21aa36337b88aaa95ecf772e5b7d38c9b33796214c9e`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dfafe96eb09e15c806e2de609acb84971f7449df95ce740199d535565a2f52`  
		Last Modified: Fri, 27 Sep 2024 06:01:05 GMT  
		Size: 103.6 MB (103611891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb963a012e2e1ec80b0afebf9b58ba6fe885c3977bb8f49037a3f42c542a60`  
		Last Modified: Fri, 27 Sep 2024 06:01:04 GMT  
		Size: 69.5 MB (69482764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3fc5991232a194dfd60fd426f8005b4edc91bc39309e2d53ebc0a94bfc636`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dad5c2a5856545ca1fac54cecb6a55dbe0b105c5c3840700e4a7120c0079c2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b052042a754b254584f3167688e0657f9fbcab65c6eb6bec28bbec7e6085fca`

```dockerfile
```

-	Layers:
	-	`sha256:2043211c531ee204a2f34da90895e35631c59d1b944c15366efc86aa2ecdd310`  
		Last Modified: Fri, 27 Sep 2024 06:01:04 GMT  
		Size: 5.0 MB (5017017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d057a4c49f6f9301187187c02e64613bcfbda0ebe756203b7d0cb376f1a212`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:292befceb3b91ed12b76d027be79b19d6f7bd7e25bf02560a27841612d068463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457f6751b0c68e9cac226b36b7e5436f1d2ba4642d5bf3fe9a027346db75b402`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe8391effee4ce0a2310333faf64259e20a76dd863e00b37d6c57ca38465d71`  
		Last Modified: Fri, 27 Sep 2024 10:16:39 GMT  
		Size: 102.7 MB (102729248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa909b0190f1d364509d8acae9413546e19ff01597e104a593ffede934733a97`  
		Last Modified: Fri, 27 Sep 2024 10:20:34 GMT  
		Size: 69.3 MB (69345387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf4180144fa29ad837e646a588fd7898343ad466118211ab37614e6e769735`  
		Last Modified: Fri, 27 Sep 2024 10:20:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04117f0de3492b0688444e13d1e610005bac62afa54944219d19b6709c4c26c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e8a40d9fe805b66a410f1e594db39a81dc8c590519178be477775287226e70`

```dockerfile
```

-	Layers:
	-	`sha256:9ec597a7d59c60610b8395811b85b429910cd1afd75a3dfcfded838fe6156a82`  
		Last Modified: Fri, 27 Sep 2024 10:20:32 GMT  
		Size: 5.0 MB (5023482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632e4edc4b4d1e3f6c69c96e9229355942a2a3be7f1b913c1b223edec43798c0`  
		Last Modified: Fri, 27 Sep 2024 10:20:32 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
