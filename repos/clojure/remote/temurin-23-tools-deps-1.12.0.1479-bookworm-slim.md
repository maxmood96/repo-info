## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:40bb9303f33be06c3d698e0fd1b7b35d859cb39b4431acd876868a70a6167f5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d89e5dfbb7c899af261e3e3c5508db4e6f6d7b7c1f74170f47a9be7d33fe07ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263877588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f2e1d75678d717c3bd0e414e7532560c28915befe58844030364e2bb457787`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698fa5dcf5401db68ee545df8a5d35c971f20c2e721927b1f24ba8b68594b91`  
		Last Modified: Sat, 12 Oct 2024 00:53:58 GMT  
		Size: 165.3 MB (165267587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402825a113ad6ab4b899f378380eed67122ca4e69b09aa5176358e2089818847`  
		Last Modified: Sat, 12 Oct 2024 00:53:57 GMT  
		Size: 69.5 MB (69482681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94173f1bca4c7fee0b1a6887d84401f319964fbc300a6dbab750ffcc9d2e57d5`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ffb1f1bbcce07a826547c42fbc70bb102d329e69feab1c4ac6397d73767ac3`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:708c34e31001ed2495a91618072e5b8a533450a5c52bf096cb30f58295083533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ee8dfa6757fc841ae2acf462cbaf3d513c9414a47aa0ba4518a0252b26134`

```dockerfile
```

-	Layers:
	-	`sha256:0b29d4e46083628ff687cbd5c49b70eae875a10a217b2f3455ce306b5df8af18`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 4.9 MB (4899844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e963d41b7c6e197958f7422b897f1cf55171d9ea81edfbd209266a47f875ec`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5725a9732abd0aad67b9109b7b1292f453e9b6d7bfd20a98bce39ceb2a9727f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb918d864dfa89d950bdbea3e86d360765af7f110b7d2dd02f741f54a2a56fd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851cc9fb21ca2ac3e3b1cefe22c283c974831b271df8829329a5ef738df50261`  
		Last Modified: Sat, 12 Oct 2024 01:33:12 GMT  
		Size: 163.3 MB (163252850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776dc9f90a57090783636b142c511ededfcd0e6370864f2165cef8145496049e`  
		Last Modified: Sat, 12 Oct 2024 01:37:48 GMT  
		Size: 69.3 MB (69345317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c53cb91a1e82c44bd65aa003137fd75b357c1742beb7bddc1ff716fef715e`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea752e380c96041f3a6dbc234d8c93ff2cd97acb5bfb496910c1e933410364e4`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65063e368b07fc979c03b059040fc05df6b8a42ecbffa5bd9d913310bbd2a162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbf2249e714d51b02d70a417978736a182568254ad4de9c0ff395253212ce9e`

```dockerfile
```

-	Layers:
	-	`sha256:db0a4fc784ac1c540c9f074985815d31015ad42e38c24b3a7c4d77ec0f4b31a7`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 4.9 MB (4904988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d89bc625e1cf3c7b19b587de5819f847146d39c1eaa59427f2fd025718a1f2d`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 15.7 KB (15656 bytes)  
		MIME: application/vnd.in-toto+json
