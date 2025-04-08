## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:509779bf5ce739fa9d7b78969c0fa483eece172d00d4806d0041ec2c096d37b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64d7399564a18e6eee2eb6502704c09b0f5e517b1b9bdb2d7e213ad19ad83241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143972131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e85ba74d204b865785aaac2c1d0344a1b989ed3ff70c7c5a81673ac645af03`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53c705a9d628ac6757c867a624798248461802b072781bb9075866143d24f3`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5c554043bfcf1ce6fcd18e1064961e3489afad622401467da3f880cba26bf8`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 59.0 MB (58992834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659be8ba725808debe79521bdfdef6cdafe241c30c49872db333218f12d4a182`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:060569fe1313c48c2605a6a616919c8c8a32eef2ce1d605df2374d80a185212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8118f552fac3a95072f7932bf7a57d21a95c7129b08dc5063f8303dbcdf0e9`

```dockerfile
```

-	Layers:
	-	`sha256:99985a344c510d9d78666b15f4416754b319d8b0c776283222d0ebbc1a3f7b52`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 5.2 MB (5240623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ae5f90288dfc190092c4f8f737358ffca99bdd1e0d7bce160842e31c68f565`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5af533ff7a36937f1b5afe3c63dc4489d0aae8dba4ef651ed88837fefa392229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141477765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b789b82d8089fe05dbd1b201cd176cfb9ebdb8bc0b4b511fafa8fb275bf3fe`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0beb154d80ddf299833a8f5c917f8e13c0c4020b2126ace13eb5937913cfc1`  
		Last Modified: Tue, 18 Mar 2025 00:11:30 GMT  
		Size: 53.8 MB (53822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679021a82ce83f4250ae2e41f1f7b1fc1793bc923458782241a44c7346cfa68`  
		Last Modified: Tue, 18 Mar 2025 00:11:31 GMT  
		Size: 58.9 MB (58908420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5be903dd04b0497e9b1d50ea5d4743a40dd1383e9a98f6f7da35503a20bce`  
		Last Modified: Tue, 18 Mar 2025 00:11:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:390d09a9ea5244d1454479bad0666bdf66b20aa79542474eef8d4148c52c5514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab171514071e399dcfa4d52e23a3480766c98ea0eaebfbc958d3d6dcf03e66b`

```dockerfile
```

-	Layers:
	-	`sha256:9222093fe68b7ba06170976b71dc7be47a954d454b27699492d6bb386a2911f3`  
		Last Modified: Tue, 18 Mar 2025 00:11:29 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5014e3281279e64d57f60edd738a7982473e2044abe6faeb87307b5b7f03e095`  
		Last Modified: Tue, 18 Mar 2025 00:11:28 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
