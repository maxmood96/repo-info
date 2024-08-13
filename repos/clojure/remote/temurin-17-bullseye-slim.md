## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:fde068968fb1f5e14acc30fc853f9b8b574bcf7c6cef8c9d8191bfb6e3cdd9d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0742cac4cb18614696a0ac7956775e938756647c8de96c600f6d4603a98e9751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235168241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b700db9c5803209b571daafab1f9d7baa2a9db5f3e8a7553e6aa1b205dd1a74b`
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
	-	`sha256:c55955c21a3614fef9cfa242dd8f7ae0cfd666b107bb0b40249c750f780a9a9a`  
		Last Modified: Tue, 13 Aug 2024 01:11:35 GMT  
		Size: 145.2 MB (145166551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3adb269d27901c5f9504e9da8f576ef8bd41cf6dcbd7ece229a2c3a62a1fc1`  
		Last Modified: Tue, 13 Aug 2024 01:11:33 GMT  
		Size: 58.6 MB (58572361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a568de852b8584c7bad92ef12bdc6d22947c846bd029249d41c9a89089198`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e189746a42b5ee4223d3ce4015aa1031121ffbf68c621a4775dde9a7373acc9`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:815f0313764f79236fcf6d49bc21aaf3108374cdb4098ef47610429acaf3a4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb221086b90ce0c059b165bf992486cadd7e27a9485646f8639e0c6fef52752a`

```dockerfile
```

-	Layers:
	-	`sha256:56bd513bf82d7ce91fee14b4e7457ce1a5c9eabf1f16e471b746a510082552bc`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f72a2234008212c988ceebd2ab0fb55a110651dd2f5bf7f98ddc3291febd79`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7a381d54898600c9859eab52369ef9e815e2f6b3d6374e3ea3af2d39d276b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232736016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf771152fe2133c1581a502bcf273438b2a0de43a49b9e8c748bec75cab0114`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c6c94bfde96f39c9817ef48cc71540647b81caced404855315c4e47530ceae`  
		Last Modified: Wed, 24 Jul 2024 12:50:33 GMT  
		Size: 144.0 MB (143959485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057638701a74f391e5b0919416b257b3c39a51e8fa5aba3f903e935e13979fe8`  
		Last Modified: Wed, 07 Aug 2024 20:09:35 GMT  
		Size: 58.7 MB (58699404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c5fd5516a056946c254502fe6ad04be825b46dcae320b85d18ec886e2f2396`  
		Last Modified: Wed, 07 Aug 2024 20:09:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99f71e8fd7400ae60d6c6fa3709d5f61830ab1db811a271951df03155bdf51`  
		Last Modified: Wed, 07 Aug 2024 20:09:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44d641a3b84e76362c8c9a7be380ddd90baeba311bc60fd8fd69bfab286c2c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428000ea8b146257bdefd61035301df15f5ab873a6506ec27711e211147aaa2`

```dockerfile
```

-	Layers:
	-	`sha256:bc8c40b4c0c45580b4afb26eeb9aeab2e4b93e1da41a31e2f076d21ac7199580`  
		Last Modified: Wed, 07 Aug 2024 20:09:33 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9610c722760f5e8f5f7a821fe7916f79cb7f86e4556d7fe200ce91b966afdec3`  
		Last Modified: Wed, 07 Aug 2024 20:09:32 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
