## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:f44b85d58e07ed12ddc88335ddd78bb48c921ea62f570be1475360775c8c59d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:05166e3ec576763c75de4b2619ec40d8af9feec9c280b00d0daa4b570ad77219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246482807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8815e8b0ce45e67588e5838687d3515360f1e1e7fb14ebd8e26b4adb976615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94dfeb6aeb6328b53d1a09965324882d4abe67001c86b538631ab10d536da56`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 156.5 MB (156481638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606a017e211f297716742480df31f91860914cedb28241384b58fd5cf25e9884`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 58.6 MB (58571840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2a153148b80c59dfc743f67f2bb9878eb2bc74064ad4f01b7c4f228bb8207`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc876467d113226d01c23a29b46517d62113f2cad95b8b8968a39ae02552ddb1`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37af8292937181257e8c0e9a09817b81f09be0ea911eab67eccc740443455ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31873b19bd62e732727327b816a7f3b5f7c99eb27463f1a9d36d383ff038ec7`

```dockerfile
```

-	Layers:
	-	`sha256:4712867600bd7974c7b5a743dd3cc2a6fe0bb79347fb71d7e0c8207c38394b98`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6101522522cfad4909badccf9a22b88aa2120aefca911c77531270bc932d98c4`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ecf1814f748f4fdfa32807afc25ca42f903db52a41c68d08fa073b9188116435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243280604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f755bf642a5cbb53b5a79cee75313042dfbe45990351dffa57eda01a65c4a55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07cd52082c604338e4496b79fa1a5548f61bc064b2a3397d681c55154f62c74`  
		Last Modified: Tue, 13 Aug 2024 06:47:17 GMT  
		Size: 154.5 MB (154503731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0604adf50431dc6908909ea0a7082bf6f0dd65437daec8b4d3198aba3333a4aa`  
		Last Modified: Tue, 13 Aug 2024 06:50:33 GMT  
		Size: 58.7 MB (58699747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcdf0508bea8d52e3cabf47b9ead0f2c282c1a5c7e65a4aa75173f9bd3f5318`  
		Last Modified: Tue, 13 Aug 2024 06:50:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21de2635c42ed0cb16e9be9efee794d007c854fd5e7a1ec169eee655480c4cf`  
		Last Modified: Tue, 13 Aug 2024 06:50:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3dd530e95b01ece49da5f82fd2479e415aa12ad87ac7abe93ecb1a71da02952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf74df4b0dcb3b48aef3cc1cd551e7771db6a141d44f35f11c57b62c34666`

```dockerfile
```

-	Layers:
	-	`sha256:bd6f6b7a90e6d85239453619d775012955ff01b3094bbe36e35f376395ea0f27`  
		Last Modified: Tue, 13 Aug 2024 06:50:31 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0201b9e8b31438995a18eb7c5dfc846eec6a2192c6d7913d667c371d3c164028`  
		Last Modified: Tue, 13 Aug 2024 06:50:31 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
