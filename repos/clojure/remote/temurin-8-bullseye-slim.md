## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:f9f8873404d1f57fadbad0dea1ea74a41cd9960e708bcb06fb9e09a19a7a4353
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:02d3b727bec5a53f02c509ae4d263812d824d40c5f5ac3b6d8c8026820768489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143746076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f574a578de8831dc54bfc2a67c1b71e4b4a5a5b488b1a88e40ac76fb5109f401`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18f1a99c5311b932320fe55b9b811309bfeff29773f29d0df1866544cfd66b6`  
		Last Modified: Wed, 22 Jan 2025 19:41:42 GMT  
		Size: 54.7 MB (54711736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3216d3541203217ce5c4e7a1f5a95b2708c79558cffd38a0dbaf3ff156980dc8`  
		Last Modified: Wed, 22 Jan 2025 19:41:42 GMT  
		Size: 58.8 MB (58781030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9b2363a3833368e0de6d346e261d61ce522dc25c77dee2c426ce168438d3bc`  
		Last Modified: Wed, 22 Jan 2025 19:41:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eaf2f1afee56ebc63c18d19c73de9faa899b2ad6a627b773dfd19c2bf9c65c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cade5253e8313c08106dc755d18a4ffb5cc2b4ee478590a9168710465546ce2`

```dockerfile
```

-	Layers:
	-	`sha256:7be64f2423d7fca3632059d2f984ecad2d0a6685467b390c5ed4e80909048336`  
		Last Modified: Wed, 22 Jan 2025 19:41:40 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c17dc9d2bd28bd96dcdd21b05a17b3828c9bb17b053a4770c121c6ba82839c7`  
		Last Modified: Wed, 22 Jan 2025 19:41:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12ae227e78095f8a036748afd8d8f64c884187c9b7baf98dfc25ad0a06a2fe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190398383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecbd647d6597e92434040b444ef2e9e1b9c39d01c4f9a219f9ff1b00b617d18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138dac51088b550996e95672455249c80cf2a82b2e2471487d2f32d2588fa7bd`  
		Last Modified: Tue, 14 Jan 2025 12:16:05 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8429554059007be98d278a199c1bd32856aabe82b3014e6b8e1b96708ef34df8`  
		Last Modified: Tue, 14 Jan 2025 12:19:16 GMT  
		Size: 58.9 MB (58905096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4aac9d24cc2714ee2e2d61d9d17aafa08f9574988c19be4ead7bb203936efe`  
		Last Modified: Tue, 14 Jan 2025 12:19:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a2c28bfc43b9e62d204e97b2dc4f668f1186f7a75621f7eaf94e3c04d5c66ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afa4143fbe7409103cf042c6dabd98e00e0e98baace0ad7e1dbdacee80ee70e`

```dockerfile
```

-	Layers:
	-	`sha256:4bc12edd36ccb4ea732bba007fc7c8ad31793aa336457c7ff7279be554bddc00`  
		Last Modified: Tue, 14 Jan 2025 12:19:14 GMT  
		Size: 5.2 MB (5245717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fc20e7f32df496cced7affbd3cbfb35dcfdb282a83665d8c2fef88ad3daf44`  
		Last Modified: Tue, 14 Jan 2025 12:19:14 GMT  
		Size: 14.4 KB (14412 bytes)  
		MIME: application/vnd.in-toto+json
