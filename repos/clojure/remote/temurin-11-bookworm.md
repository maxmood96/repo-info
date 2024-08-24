## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:243d590ac406663ecd81563b45c549b653c906a5f0889cb7b930da8a457722f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:93b6101ea67a1ac30579a64b69de3558668a0048a464dc1091b63aa5541a6d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275558225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215c0a2fc5efea431a95bc6c2a89ebb392081dc51ed57db9c56343fb09fd9db4`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09310bb4cd67d2c499d38a26870861dbc5200e025422c902d05de75beef0175`  
		Last Modified: Fri, 23 Aug 2024 20:02:13 GMT  
		Size: 145.6 MB (145550028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72807e4ebad18ff592bba6a74dca4bd15afb5c650749f455cbb132443f67593b`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 80.5 MB (80453471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250a414a3944cef3397ac14c566b1af7ac05d36238bada0b237708019ec38c1c`  
		Last Modified: Fri, 23 Aug 2024 20:02:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:21db2ff7b221280d09dd5682c8232bb72adcaf47b78e0016a83d5b5c53869324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b16d364ca4213a6ee04024faecd5000f4b91e89b9b16d76c564bba706735c`

```dockerfile
```

-	Layers:
	-	`sha256:918985c8b3b5146903a1c5d291eca866b016930223c89158bca1962c76d61c43`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c5fde994c76b5882d7b5bee7533f642489f7922f9d972630d61f2eadc7b711`  
		Last Modified: Fri, 23 Aug 2024 20:02:11 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75f6863cd5aa6325d4a5967344ebeb5a2c80d0bb35c1ef0e5df31837b5b208f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272142290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f0b8788161c1e6fbee0e79cb8e87b84be6e437ec1cda1bf0b4e10b486a557e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c7e107b4736e704c136824cd4b625750da0fdc9e8e5ad885340c116db3e802`  
		Last Modified: Sat, 17 Aug 2024 06:01:13 GMT  
		Size: 142.4 MB (142354796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a028f297c3ae77df2154f3ab6b69bad87ab2a7b467d4e33fb8a55dd419e0110`  
		Last Modified: Sat, 17 Aug 2024 06:06:37 GMT  
		Size: 80.2 MB (80198257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9978749ec473fd97049acdb7c3242b48466a2975ad13a479c11807e234c8f9`  
		Last Modified: Sat, 17 Aug 2024 06:06:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:302b843c340f8438ed106c00758db7be3ab9a63feab94e86c9fe140e88011a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf8f8a8b03a9a2e1fa828425e1335b6b3e059ef302cc8baec90a9c38b1123e9`

```dockerfile
```

-	Layers:
	-	`sha256:7df0690bf77939fc6432d08ad7560d4da858f6da5fe665e504082b6b0270cd26`  
		Last Modified: Sat, 17 Aug 2024 06:06:35 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df0354e98da35a52bd8a24a6b2c4d488497a8c1512525bf2a227b3f2588336c`  
		Last Modified: Sat, 17 Aug 2024 06:06:34 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
