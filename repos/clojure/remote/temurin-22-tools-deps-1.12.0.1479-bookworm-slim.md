## `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:65717a41a63e6ff25ca5612ffcdab9cc252f7b4f403358184731bcd50c0b787d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfa8611611a6e24af07682a64dd4ce63a93cbc82e81188798eee3d04716c8989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255091699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0dd8b8e62114e626b3929f1ccd0ab61a53d5c7ce4ea79e76cffecf0e1b7a6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c4b4341317ce78e2386faf285086f80975eb89b15250f1cee5003297f5873e`  
		Last Modified: Fri, 27 Sep 2024 06:01:25 GMT  
		Size: 156.5 MB (156481613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6190a9957f04c91762fa01ccb4394048e6d169cb22b2a9b4215457b0fdf24551`  
		Last Modified: Fri, 27 Sep 2024 06:01:24 GMT  
		Size: 69.5 MB (69482773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05895ca1ef7f9dd707f8b9ad22efb724b53afef8e7640fd67ee1c65df6114262`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a59ab7a1c1a072976852228bad6b283c729d6785704eb0f4380421240f9db`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d51a4eec9ffdb17e562bf58970ae673c9408659514f6f8ded840e6c8f2937bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4519348cc8ae1f0e278a71b66e2b053c19bdb53aaed40694464520debe0b9403`

```dockerfile
```

-	Layers:
	-	`sha256:4ba26c172e4d2b0035d5a897ad2db3244d9726c0ea1440006437e6ea953daa88`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 4.9 MB (4898554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a9b891b1bc6bb17ad6f730f6c856e246d485751a0e0d8017cd415730487f96`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb3199f04e663fb8e742aa78007a9e7e36882a7acfcdd1b23fee80c210d5d12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253006071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408eee90554967a2d05cbea13dc810764d28536b3ddd62088be79434878cec01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e89b3773177f335767b4229a846a6c6a6c40fe88056e5a9a0582698d87c8bbc`  
		Last Modified: Fri, 27 Sep 2024 10:47:33 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd8f1fd696e501342e50725a8059c06b413a753bce23a726472210498a954e`  
		Last Modified: Fri, 27 Sep 2024 10:51:21 GMT  
		Size: 69.3 MB (69344907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392690472d51c80ab08958ffc981781d42d91dada9fb7310560954bd34d93d06`  
		Last Modified: Fri, 27 Sep 2024 10:51:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14adfe2b7719786a3093b53358d36c33a12004d9b65e1dbc6562a2d37d3e853`  
		Last Modified: Fri, 27 Sep 2024 10:51:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e48fa54845cc35320a8518afb320a85f7d0bf3b0b9aad5aebfa1c7ae4ff201e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4919752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48946e82cc59002ef576a2a633cd8369428525120add68d5fc87de4db8680e38`

```dockerfile
```

-	Layers:
	-	`sha256:056406e3d0f6bc934e89c8340003f399a4321bd2ca406895aed4dda8f888770c`  
		Last Modified: Fri, 27 Sep 2024 10:51:19 GMT  
		Size: 4.9 MB (4903698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b668de85bfb1f89927948395daa5b988229b2151f6f006940923db30c1520d7`  
		Last Modified: Fri, 27 Sep 2024 10:51:18 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
