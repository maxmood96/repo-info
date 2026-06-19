## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:1be3549c9d62281ad820c1257bb70ecd796ed21ba0c2291918395674f9836011
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dd749023b215d22702ddef466e8a1ad98c108459231c076452ce24f1e8b18307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266190906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a4c896c8f38cfe8ac91e507ff95f15d27707c67bc8d50966131bfbb953dec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7828dd2cfcf145bd85f23822277d2e4cdb24d6966dc68457c99cb74670ca15`  
		Last Modified: Fri, 19 Jun 2026 02:17:58 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad451ce69e1a934dd511c64dac18942c886d935541ab02d7c9d678e0c79a2e0`  
		Last Modified: Fri, 19 Jun 2026 02:17:56 GMT  
		Size: 66.5 MB (66512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b2ca0e7dc3eb44ee31c50dd4827169df2b8f853c4c1d9c3fd495e71fafa08c`  
		Last Modified: Fri, 19 Jun 2026 02:17:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a79746065ca2dfeb136ba74403c89cfd3a6347cbbb0b9b42486c881cdf575`  
		Last Modified: Fri, 19 Jun 2026 02:17:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ddba49c207380a6a21648bb8e46cb3af18b72e626d9080ead42b546e8862d276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616d366b8fbd662421832808efe04bbce5660e00a544b7bd61a5e0038c32b972`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e2c6f536fc240160fc26395e09fffe0f318f84ebfe3c4669b7cb3791db209`  
		Last Modified: Fri, 19 Jun 2026 02:17:54 GMT  
		Size: 7.4 MB (7407073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd7b5b0253fc1bb86da1f78f0c9d5cbf7784f99f18b405f21bf1bf9444f04f8`  
		Last Modified: Fri, 19 Jun 2026 02:17:53 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d01f0392dafa8f586a6226e2f9b4941ea1d1986a24d72ad60cd8773aef149780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263667406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86f28f10aec541c09d284c521332aff183e4f62546c7820c8fd87fb70adc4ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975a72c18d4838a8b0a08c75f74565b032964fb6a348c03ba7525b2a0590d53a`  
		Last Modified: Fri, 19 Jun 2026 02:18:15 GMT  
		Size: 144.7 MB (144724318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d518519de8d40e1f33ab613ecda61f83ad160af4a39b2baefc61f82c9cf88af0`  
		Last Modified: Fri, 19 Jun 2026 02:18:13 GMT  
		Size: 66.7 MB (66677931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723078a45a86937b77946f71f873f234583966f88192b14b1c698131be132c65`  
		Last Modified: Fri, 19 Jun 2026 02:18:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257ef3a71e5151380271994a4c73bc1fdfed7b3af83dd53856ba8b48777c86c6`  
		Last Modified: Fri, 19 Jun 2026 02:18:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:438a2f806370e8f9205abe0408d729cf1236eb5fc01e0d968324746033d26faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50699c94fcd014dedd0ce396a54eeb7e04af53ec96eb6a90bd777b29c8e77dc1`

```dockerfile
```

-	Layers:
	-	`sha256:219dd33aafc82b2609315a1d3432325c0dfad8bad3f96e46bec3dd5e48baf707`  
		Last Modified: Fri, 19 Jun 2026 02:18:09 GMT  
		Size: 7.4 MB (7412172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c10a188734a9883af039642542dd748a7420cb546a3e83aaeb58da87b2c2a53d`  
		Last Modified: Fri, 19 Jun 2026 02:18:08 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
