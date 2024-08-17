## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:eb9d34db75433dce7e1f0eef9e1dd6a43da8fc5275d168eccb5e9ef54b8dcc16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:23867dc6e4cad5f478c0280df0b46bdd689cc35f4976485413017481b54c295c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275558870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123e26b68f0da4060f33a600bfc88260563e0958d709dd1892eca26397b2fe0`
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
	-	`sha256:9ea2653587b7d229ed21829f02a7442f1d67df7b82193e5458569c43e33cc629`  
		Last Modified: Sat, 17 Aug 2024 01:59:36 GMT  
		Size: 145.6 MB (145550113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c615569d1d176b4dd88124375d6631ccca8ff1984f34f68414d797182ec83ae`  
		Last Modified: Sat, 17 Aug 2024 01:59:35 GMT  
		Size: 80.5 MB (80454031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566377ab71280db36fce5d2bf7d7f35858bb5a798d68fb442a0b256ea0ebc9d2`  
		Last Modified: Sat, 17 Aug 2024 01:59:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:000affac262d4c916ae802cccd12af1c578a1b65ae469ec2f037daaf767200e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468549f6a67e8f9e128247fcba2eaa351b669a040b9b0af803bde7c313dda194`

```dockerfile
```

-	Layers:
	-	`sha256:d22ad3f72118b6552f64dc89beae48abb34d3bd3a7e376a2d9c12249dbb7f19c`  
		Last Modified: Sat, 17 Aug 2024 01:59:34 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7486420587fea7e2dcfa2d07740a6c3340d3e83659731a46df08af557157d25`  
		Last Modified: Sat, 17 Aug 2024 01:59:34 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5589b9793069e3b2e5d5fb2ba2fe9dd8cf9e93d56518571dead3b592c2432169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272143976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db448ec84dfd667611ce04d182df0fb446a01ef5feac0fd0d697bd1f1155dcf3`
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
	-	`sha256:968d0608f53de4e65cc57e56ba039f3214ab357a0f4c22a6c784f589cc0a3009`  
		Last Modified: Tue, 13 Aug 2024 06:22:46 GMT  
		Size: 142.4 MB (142356407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075416673a87e05409f828583c2cdb912d8595977e4af07dd501fa013721166`  
		Last Modified: Tue, 13 Aug 2024 06:27:19 GMT  
		Size: 80.2 MB (80198333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d81c0dd4f7147a43c0ecce4cf9bd110d468638ad046b1a40da5c0f6b22294`  
		Last Modified: Tue, 13 Aug 2024 06:27:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:17b185ab65e1d4a3d017b3074e32c7511d7c1d1c85cc4b34893f133ed3845b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322c582c07253f1fdc8a520c307e5309796f6b8944bb44596e85bebdaa76c324`

```dockerfile
```

-	Layers:
	-	`sha256:02a777a9618e15630050256809c10715097bcf0ed38b93cb71de331b15c4e4b6`  
		Last Modified: Tue, 13 Aug 2024 06:27:17 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac34f20759a9f98a8b11963b214dd68cfa117cfef914996053bdf161b934ed5`  
		Last Modified: Tue, 13 Aug 2024 06:27:16 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
