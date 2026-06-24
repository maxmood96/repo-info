## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:ed17a7be15952caf4e5d6bfe01eb3e20e93e80976b3ea88a619f58e381f33be2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:62da915ec137b06d5cb4e2152469f1c9c94ffe1a274244789555afade721515d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187035403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abdf99894a87e350e1d1ef42732f4566cae4c511e1e947e2c575b5e546d806b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:14:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:45 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:15:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:15:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:15:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ba20eda01da6cdfd88d31ff8f002d79e3fbea3809dd50bf8881292c7d9209`  
		Last Modified: Wed, 24 Jun 2026 02:15:22 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e78758f70db572e2ad98845c43f24395837733040e56691dda6e64531be383`  
		Last Modified: Wed, 24 Jun 2026 02:15:22 GMT  
		Size: 82.5 MB (82518776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef4a47cb504899a87a98c70b204eb30b9dd95c4c06e5d1075f517206b47f226`  
		Last Modified: Wed, 24 Jun 2026 02:15:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bf86c3c442dc864edb889fb91683a96e0a3f276c6cb1a20e8f84229cfc32367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38fa9e51a5ca86818e2100dd84394d60fc9d97363093853e4c9bd1612b30c34`

```dockerfile
```

-	Layers:
	-	`sha256:f9864df8aaae31e8a7a0a7feada0368d9a9cbeae17c10e508e29e4210851c8ee`  
		Last Modified: Wed, 24 Jun 2026 02:15:20 GMT  
		Size: 7.6 MB (7589131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a92d027197bccb9d46a7c8debfa9e3ed6343234c7ef17da3193634cd67a429a`  
		Last Modified: Wed, 24 Jun 2026 02:15:19 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfea1995854f5b5f39ac9674d98487d6ad3b2b3d262df494536eda24707b93c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353100740115c5886677eea533a7128a72a6203ab5cce8b25c849d960687ea7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:21:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:22 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ddbedb924e20a8966da6854c255cb3d38b1b857f1f6aa023d6b5b91522cefd`  
		Last Modified: Wed, 24 Jun 2026 02:22:00 GMT  
		Size: 54.3 MB (54272910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06decdf49b15d8687b49ead478ee29da503d877bb0d0d4bc642fc63336d3b815`  
		Last Modified: Wed, 24 Jun 2026 02:22:01 GMT  
		Size: 82.3 MB (82338108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94900223bd571a510aed77e6d37c8b4ca19462ae4f83f6977dcf6e4f13c22116`  
		Last Modified: Wed, 24 Jun 2026 02:21:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:13faf930d14c0680acd9684b6c3d4c3508cca1d012afca34e467703cbe98f998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbd059a6031c67ca04d3f1a3c28cc806424d75c3d858776c43b5026ad86d86`

```dockerfile
```

-	Layers:
	-	`sha256:e32406870a824bb8ff23d2c3f232a092c08a1144d8f2ced8cc536a811c214f99`  
		Last Modified: Wed, 24 Jun 2026 02:21:58 GMT  
		Size: 7.6 MB (7596224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd89e648e64cd499f88445fa0878902ffd78f3b81800f1a7f8e22fc8bc3b84f`  
		Last Modified: Wed, 24 Jun 2026 02:21:58 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fa8f4cbd4394fe252af76aa90a26c0701348dabeae07282aa1821f68e42c01ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193746732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575d6b411a3e1a55b59a89657639e85d026c6e150bbf960a28cd625ad76a664f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 07:49:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:49:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:49:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:49:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:49:57 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:50:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:50:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:50:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63759de38e2ccf9f09021264563d90edf72e1fb469886cc56f717f750a614fd`  
		Last Modified: Wed, 24 Jun 2026 07:51:24 GMT  
		Size: 52.7 MB (52669138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d740f75789cae3c2a4db3a6d58edf00806d8e92221b57d40aa72ac0a302c972`  
		Last Modified: Wed, 24 Jun 2026 07:51:25 GMT  
		Size: 87.9 MB (87938879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651616d83ebe19cce10abee8c258b863b6645a40a9af7736e245d7519c4e8b6e`  
		Last Modified: Wed, 24 Jun 2026 07:51:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0dd98d48832383b5f0b7f9d3076e71b258e58b1861779c0777b4265052be9b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd573d7b36a73af3637f579aa106d558b6832b77a35a82294c68cb46573b65a`

```dockerfile
```

-	Layers:
	-	`sha256:e5cc1125d00ee15fd5b31c0a2ba3f6bcd0204a43af8979c87aaa77e0d5a3ffb2`  
		Last Modified: Wed, 24 Jun 2026 07:51:22 GMT  
		Size: 7.6 MB (7594147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7881630d0ed30aa1e1a3cc07680accabb710193a0fe959af42f67641b8dd30`  
		Last Modified: Wed, 24 Jun 2026 07:51:22 GMT  
		Size: 14.4 KB (14372 bytes)  
		MIME: application/vnd.in-toto+json
