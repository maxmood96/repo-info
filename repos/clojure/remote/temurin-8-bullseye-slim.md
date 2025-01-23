## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:a329fcf64718d4a95118e2b3f17c8d08011246574bdeeab6eed6349ba74f382f
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
$ docker pull clojure@sha256:5354be50a6691755d255cc1136bc52461a3f0ad4258221ddba0cf9a2662fff11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141467217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccefb8abf197a31cb557c41bb37954965e14be0ab651e2e4df535695b2941f7`
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
	-	`sha256:9d98c3b0df4d7e43fddbb9464d103364cdebc6bb3887c057766dc088321ed2cb`  
		Last Modified: Thu, 23 Jan 2025 02:27:53 GMT  
		Size: 53.8 MB (53816395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb052867e7df4fe763f022a39cf7eff0a761ab78e0f45578e42ad7aadf8790f`  
		Last Modified: Thu, 23 Jan 2025 02:32:30 GMT  
		Size: 58.9 MB (58905263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9a59f4cd32da346a4e8b02bb3cfbfcf85e1ba9aa3123aeb6a1d5c15e2b411`  
		Last Modified: Thu, 23 Jan 2025 02:32:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:801c2f32fdcae1bf3f2fbd22efcbf5538eef99373efb384d812837342fbcd1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4fdfe03a3c00798ecfd8f25c17e12e782e663640413680b023a706e65d4f2f`

```dockerfile
```

-	Layers:
	-	`sha256:961321f277c86aa29f7e93009615d43eb06739f99723e3705348f6a60c02bdd7`  
		Last Modified: Thu, 23 Jan 2025 02:32:28 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c575d4362bd9b69c965425f48ce1263c84ee45ffb95179e799a0d21fc61f4a3`  
		Last Modified: Thu, 23 Jan 2025 02:32:28 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
