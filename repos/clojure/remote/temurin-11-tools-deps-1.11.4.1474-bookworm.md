## `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:4f32a5ce6562de0f1b07a9584aa5ec950a25b31d1c6616fd1aaf66633ba178eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:948353c1bd3ac731050c70053588a97cbda16727dd364e9f7cb58686c5971752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275573590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e347d60aac5baa797e74d24564c0c038f58778f4acfa3c78d6ad0ac417d91035`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f8599f5ed5fd65a4b1e10ef5faa6cfd1b66a037bd4781a1f8a54830993d21a`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 145.6 MB (145550053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aec33bcde127949ff3561fe22ad79fd68cbca4cafc5d95ee33c3f61a651e9eb`  
		Last Modified: Wed, 04 Sep 2024 23:07:47 GMT  
		Size: 80.5 MB (80466190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e384ff85003e77e36a3f1c3c4bbe54e69a020108d1b4af212e0c8f8e0dc37f79`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:07d0f26670d1b3a3724b3a4bf50fcb516edf5a6689bc1f74fd9739f5c9dc94ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beebd9d28a54ed987c841b0508d259a34cdae0fe3475479eb53cc52f0bd0909`

```dockerfile
```

-	Layers:
	-	`sha256:50d8c7093a282ac49981563bcdb8517724e96f9231ab2de5e21bc859bbedf4f6`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7d6ec07e74d498746f1df43252ad42912bf57072e687061ad144947fe4a974`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:715e6c35701adecc0dd7c9cca7af159c95a0d71fae8e4452f995303ceb671fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f877a52082781a18ab201ef7c7384edb154b876f4f3d2d54e9f5cefe8488184`

```dockerfile
```

-	Layers:
	-	`sha256:f8c08c56d5935f99bf7ae39485987ccc43931e15f1959b1826f4f5a866908587`  
		Last Modified: Fri, 23 Aug 2024 23:54:13 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98bb21b691899461aad27578af8432407b4be00ef2d7f1cfd9f51697704c007d`  
		Last Modified: Fri, 23 Aug 2024 23:54:12 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
