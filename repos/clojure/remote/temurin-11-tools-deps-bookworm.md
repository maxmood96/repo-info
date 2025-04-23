## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4a820d11977fe969c3406ed6eab300237cd3e577c042c4235da78b904f00372f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f5fcbda6801783b8b4a4d8dc93c91dc2ab60962de7e3b685b7a6a75047e36b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277427666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195cd2e12758f4ebdaa9ad133c4365d423e3054eb79b6c5c6a5c7c2117b93569`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdacd2bba554949e85c451e3ea78d20039b927e50efb984d6610f0f19b742e`  
		Last Modified: Wed, 23 Apr 2025 17:15:43 GMT  
		Size: 145.6 MB (145635867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77e9a948b8fc80516bd4ef789b0c8af7b31ff11f234bb9f8dd733895d692df`  
		Last Modified: Wed, 23 Apr 2025 17:15:43 GMT  
		Size: 83.3 MB (83300609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e560bea477d12c87315dda1825d9acbc1a7b4ef526139f06905262e0abc85a70`  
		Last Modified: Wed, 23 Apr 2025 17:15:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0b1043c8855ec145338a8e56176374521d6f96bd85e21e603d4068260fef9ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc820677390775dbcd9b99476b771d354f320e06c37ffa9610ef8f0c9038d589`

```dockerfile
```

-	Layers:
	-	`sha256:19b2e2a49cdeffb99904106fa96d801e44092fc54dcd27fb3970fcd36ca71297`  
		Last Modified: Wed, 23 Apr 2025 17:15:41 GMT  
		Size: 7.2 MB (7192617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c27c4c828cd9014749cbc957eccd21ac9efd9645a15325139dc282a288eee0`  
		Last Modified: Wed, 23 Apr 2025 17:15:41 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad64daa79af3d3077ab6a1a9b7c66bf2ed4d998e68a9044522cdca632b886a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273868553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5e9d83de56b6f0a817a14c5f946fbc3e1751a554c68791819320cc42ede029`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c300f0d53d6e4cfe9ff27815901c6e0e09debd96a763f2a8b622880dddc87f`  
		Last Modified: Wed, 23 Apr 2025 19:35:57 GMT  
		Size: 142.4 MB (142422092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d367f1379895e0cacff55dd7cf40a089973d2b9d8973894a783b8014b9a9f7d8`  
		Last Modified: Wed, 23 Apr 2025 19:41:10 GMT  
		Size: 83.1 MB (83118347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a77ec133ed7d078ded888367132820d45e851b1e10d2f5596d471089c391e3`  
		Last Modified: Wed, 23 Apr 2025 19:41:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:41b0fae6736b84957d74d48f96ddec154a73e5165b149c290042c1054ec77140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db46e9ea27c384668798a26cf9590c3c3fc8f70b6e0b9760e2dc264a193f478d`

```dockerfile
```

-	Layers:
	-	`sha256:938629571f79ebb97057b53ec7593ad570d06258d64e9f8162c77606ab4b50ca`  
		Last Modified: Wed, 23 Apr 2025 19:41:08 GMT  
		Size: 7.2 MB (7198998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d789a52c0dee1cb6f030028a1145492473bbb8089d3295fbaeeb70e781588dc8`  
		Last Modified: Wed, 23 Apr 2025 19:41:07 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
