<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.30`](#neo4j4430)
-	[`neo4j:4.4.30-community`](#neo4j4430-community)
-	[`neo4j:4.4.30-enterprise`](#neo4j4430-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.16`](#neo4j516)
-	[`neo4j:5.16-bullseye`](#neo4j516-bullseye)
-	[`neo4j:5.16-community`](#neo4j516-community)
-	[`neo4j:5.16-community-bullseye`](#neo4j516-community-bullseye)
-	[`neo4j:5.16-community-ubi8`](#neo4j516-community-ubi8)
-	[`neo4j:5.16-enterprise`](#neo4j516-enterprise)
-	[`neo4j:5.16-enterprise-bullseye`](#neo4j516-enterprise-bullseye)
-	[`neo4j:5.16-enterprise-ubi8`](#neo4j516-enterprise-ubi8)
-	[`neo4j:5.16-ubi8`](#neo4j516-ubi8)
-	[`neo4j:5.16.0`](#neo4j5160)
-	[`neo4j:5.16.0-bullseye`](#neo4j5160-bullseye)
-	[`neo4j:5.16.0-community`](#neo4j5160-community)
-	[`neo4j:5.16.0-community-bullseye`](#neo4j5160-community-bullseye)
-	[`neo4j:5.16.0-community-ubi8`](#neo4j5160-community-ubi8)
-	[`neo4j:5.16.0-enterprise`](#neo4j5160-enterprise)
-	[`neo4j:5.16.0-enterprise-bullseye`](#neo4j5160-enterprise-bullseye)
-	[`neo4j:5.16.0-enterprise-ubi8`](#neo4j5160-enterprise-ubi8)
-	[`neo4j:5.16.0-ubi8`](#neo4j5160-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:a887d95dbed7133a1ecfa2d993c5da7578445628598c0a545ae605a6923e4cc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:3b872f8a79c2663c6d0da2c897a9e6df5ee9ac24d89576802250a576482eb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bab9eac802fe02f7fac68a579d10a5cd1ea7cf2f0d0cdc8f57ecb816f2ae3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de4a807514944014b664fda8c4dc4237fb059cf1e98231ed1236554a87c7bd`  
		Last Modified: Mon, 29 Jan 2024 22:52:31 GMT  
		Size: 145.3 MB (145271181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401735ad1c9f9c2fa33dc320ff727b2b3e52becdbeb1dcf1ea01013adc65286d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b0853394b64f41eca44c431ee2e7e5b1ef255321b79eec5a693e829cefde80`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72610f3f1e6b5ba11994b2dc95e5383a844ecbffca8430efed7529e5b87f53b2`  
		Last Modified: Mon, 29 Jan 2024 22:52:33 GMT  
		Size: 120.6 MB (120581594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:5c6f5496a8f31c956351043882d567410c3568758bc01079a5bc563b0773ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ed2f90620a7a3efedc540af3123a18dabe015a9878c06411a4cd08cab346b`

```dockerfile
```

-	Layers:
	-	`sha256:7c54c2279da650a4561f549e2ed5ee921551a93efb859932b72d9514b5ddb3a2`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68af72f16453a3eb8e0c275788d57c8c6ba85a842742cc27636dd9f201e3dc3d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:05f4a9612e1f831ee0ab26ec8c59ae498267aef71a3949115b164bea7507c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d305f54aad2b8db44d03474e5155cfaf30dd8a8b5c5dabdca82a0a250ff1c2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dcac7d4d68c69b3693e8d1b796cb529cdb38fb41555613d24b0a7e38a92b74`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f812e356d565c8c4ec8076932f10549407639030260c467c96d4726a883439`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04959ff06f5315ca730a9cfba712a8e00d2221a04c13033809e71ea267bb2a3`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 120.5 MB (120547601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:5631ad910a888b82aba59d281fc1fc1079c79e09e2346a8ab856b1a0556fe22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c07f786945aca5d5765d68743176fa83270336aa5d168d010162cca2656851f`

```dockerfile
```

-	Layers:
	-	`sha256:bd8c88a2e52536f1eb3df93ac96797c4161d0b9a9971ccf07be4bcb4e0f40d14`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 2.5 MB (2480756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae104f3c9997741edf1dbac1ba0e551642990ca6c212fb2b96d27c6763b6d4`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:a887d95dbed7133a1ecfa2d993c5da7578445628598c0a545ae605a6923e4cc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3b872f8a79c2663c6d0da2c897a9e6df5ee9ac24d89576802250a576482eb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bab9eac802fe02f7fac68a579d10a5cd1ea7cf2f0d0cdc8f57ecb816f2ae3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de4a807514944014b664fda8c4dc4237fb059cf1e98231ed1236554a87c7bd`  
		Last Modified: Mon, 29 Jan 2024 22:52:31 GMT  
		Size: 145.3 MB (145271181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401735ad1c9f9c2fa33dc320ff727b2b3e52becdbeb1dcf1ea01013adc65286d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b0853394b64f41eca44c431ee2e7e5b1ef255321b79eec5a693e829cefde80`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72610f3f1e6b5ba11994b2dc95e5383a844ecbffca8430efed7529e5b87f53b2`  
		Last Modified: Mon, 29 Jan 2024 22:52:33 GMT  
		Size: 120.6 MB (120581594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5c6f5496a8f31c956351043882d567410c3568758bc01079a5bc563b0773ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ed2f90620a7a3efedc540af3123a18dabe015a9878c06411a4cd08cab346b`

```dockerfile
```

-	Layers:
	-	`sha256:7c54c2279da650a4561f549e2ed5ee921551a93efb859932b72d9514b5ddb3a2`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68af72f16453a3eb8e0c275788d57c8c6ba85a842742cc27636dd9f201e3dc3d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:05f4a9612e1f831ee0ab26ec8c59ae498267aef71a3949115b164bea7507c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d305f54aad2b8db44d03474e5155cfaf30dd8a8b5c5dabdca82a0a250ff1c2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dcac7d4d68c69b3693e8d1b796cb529cdb38fb41555613d24b0a7e38a92b74`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f812e356d565c8c4ec8076932f10549407639030260c467c96d4726a883439`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04959ff06f5315ca730a9cfba712a8e00d2221a04c13033809e71ea267bb2a3`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 120.5 MB (120547601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5631ad910a888b82aba59d281fc1fc1079c79e09e2346a8ab856b1a0556fe22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c07f786945aca5d5765d68743176fa83270336aa5d168d010162cca2656851f`

```dockerfile
```

-	Layers:
	-	`sha256:bd8c88a2e52536f1eb3df93ac96797c4161d0b9a9971ccf07be4bcb4e0f40d14`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 2.5 MB (2480756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae104f3c9997741edf1dbac1ba0e551642990ca6c212fb2b96d27c6763b6d4`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:1c58c06aa26b49a7548c046d9838d647e8abeb9778328422e8af21d82df74f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7f57d28b4204c65ce716451f63e47d371e553222221cbb94b58273c9bffecc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402496166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11fd4052b4a057a45f22606fa41fe93f44ef48307e75a309b37f0be943e8204`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8959ff830f40bd981a6656c70c62d82e57efb7264dc98efd67d3ef1e5901b5d4`  
		Last Modified: Mon, 29 Jan 2024 22:52:40 GMT  
		Size: 145.3 MB (145271190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4262a7cc67cc0be1b04687679f1122ec38ea86bb5e0019be8b62d9f5315f48e4`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3922c318378bb4724fa889bdd01f68f91af6aa6567400b7f25f4dd058e1358`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfa46e8d6bfe31392cd41dda090b456c6dd5fb63a344ccb5e71bf642b7f6e9e`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 225.8 MB (225793771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0238794400af57589b4ea6dce6d190d14767c9dac25e67b3c5067f79e47c9a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fc5837110e4b5fcbaf01c724f39e06910c77826092b4c0e72c3639f8d0848c`

```dockerfile
```

-	Layers:
	-	`sha256:0afe6dd5108fd5e8ccb1dd4dadbd0611dbfa83ac00c8707413943a1d2f83472d`  
		Last Modified: Mon, 29 Jan 2024 22:52:37 GMT  
		Size: 2.6 MB (2598523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c909219396711881c16766588a7cf0fefe4087c534bcd49e4bc78f118352780e`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f84d4f4aef9182214e0dac1dacc883e7e26a77769702b6b00e1c87e2c725f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397841376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75ae9a21f54f187d746da19c1cc7e930fde90618063400755dbebed3561b08e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef3ca9ea8731e04c8da5e442141e100681554eae5d28f751ac4dc01d10908d2`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aec422c866c88ef0ccd93a37e679734bb6c8863671cf949555337df4409783`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541772c0b1ddf548665c4641467e804578c562cfc3976838edff3f8b4ccab3b8`  
		Last Modified: Tue, 30 Jan 2024 01:06:51 GMT  
		Size: 225.8 MB (225757447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b8b597a08e8b2dec316a0ca3c7b8f16854766be938793d74b5b375bb32b38a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5988385128dc2563c31f60325731259e1aa7a35f54b201b496d37a8a85e3c925`

```dockerfile
```

-	Layers:
	-	`sha256:6d53dbb39ab119cd04300c99bdf29f270c820e59105cb460e00400ab528680bb`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 2.6 MB (2598845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de2fd26631fd07f06983d27c955efd6379f4a4cd4b301c312d15c0a4dc82964`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30`

```console
$ docker pull neo4j@sha256:a887d95dbed7133a1ecfa2d993c5da7578445628598c0a545ae605a6923e4cc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30` - linux; amd64

```console
$ docker pull neo4j@sha256:3b872f8a79c2663c6d0da2c897a9e6df5ee9ac24d89576802250a576482eb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bab9eac802fe02f7fac68a579d10a5cd1ea7cf2f0d0cdc8f57ecb816f2ae3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de4a807514944014b664fda8c4dc4237fb059cf1e98231ed1236554a87c7bd`  
		Last Modified: Mon, 29 Jan 2024 22:52:31 GMT  
		Size: 145.3 MB (145271181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401735ad1c9f9c2fa33dc320ff727b2b3e52becdbeb1dcf1ea01013adc65286d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b0853394b64f41eca44c431ee2e7e5b1ef255321b79eec5a693e829cefde80`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72610f3f1e6b5ba11994b2dc95e5383a844ecbffca8430efed7529e5b87f53b2`  
		Last Modified: Mon, 29 Jan 2024 22:52:33 GMT  
		Size: 120.6 MB (120581594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:5c6f5496a8f31c956351043882d567410c3568758bc01079a5bc563b0773ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ed2f90620a7a3efedc540af3123a18dabe015a9878c06411a4cd08cab346b`

```dockerfile
```

-	Layers:
	-	`sha256:7c54c2279da650a4561f549e2ed5ee921551a93efb859932b72d9514b5ddb3a2`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68af72f16453a3eb8e0c275788d57c8c6ba85a842742cc27636dd9f201e3dc3d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:05f4a9612e1f831ee0ab26ec8c59ae498267aef71a3949115b164bea7507c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d305f54aad2b8db44d03474e5155cfaf30dd8a8b5c5dabdca82a0a250ff1c2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dcac7d4d68c69b3693e8d1b796cb529cdb38fb41555613d24b0a7e38a92b74`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f812e356d565c8c4ec8076932f10549407639030260c467c96d4726a883439`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04959ff06f5315ca730a9cfba712a8e00d2221a04c13033809e71ea267bb2a3`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 120.5 MB (120547601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:5631ad910a888b82aba59d281fc1fc1079c79e09e2346a8ab856b1a0556fe22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c07f786945aca5d5765d68743176fa83270336aa5d168d010162cca2656851f`

```dockerfile
```

-	Layers:
	-	`sha256:bd8c88a2e52536f1eb3df93ac96797c4161d0b9a9971ccf07be4bcb4e0f40d14`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 2.5 MB (2480756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae104f3c9997741edf1dbac1ba0e551642990ca6c212fb2b96d27c6763b6d4`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-community`

```console
$ docker pull neo4j@sha256:a887d95dbed7133a1ecfa2d993c5da7578445628598c0a545ae605a6923e4cc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3b872f8a79c2663c6d0da2c897a9e6df5ee9ac24d89576802250a576482eb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bab9eac802fe02f7fac68a579d10a5cd1ea7cf2f0d0cdc8f57ecb816f2ae3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de4a807514944014b664fda8c4dc4237fb059cf1e98231ed1236554a87c7bd`  
		Last Modified: Mon, 29 Jan 2024 22:52:31 GMT  
		Size: 145.3 MB (145271181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401735ad1c9f9c2fa33dc320ff727b2b3e52becdbeb1dcf1ea01013adc65286d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b0853394b64f41eca44c431ee2e7e5b1ef255321b79eec5a693e829cefde80`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72610f3f1e6b5ba11994b2dc95e5383a844ecbffca8430efed7529e5b87f53b2`  
		Last Modified: Mon, 29 Jan 2024 22:52:33 GMT  
		Size: 120.6 MB (120581594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5c6f5496a8f31c956351043882d567410c3568758bc01079a5bc563b0773ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ed2f90620a7a3efedc540af3123a18dabe015a9878c06411a4cd08cab346b`

```dockerfile
```

-	Layers:
	-	`sha256:7c54c2279da650a4561f549e2ed5ee921551a93efb859932b72d9514b5ddb3a2`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68af72f16453a3eb8e0c275788d57c8c6ba85a842742cc27636dd9f201e3dc3d`  
		Last Modified: Mon, 29 Jan 2024 22:52:28 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:05f4a9612e1f831ee0ab26ec8c59ae498267aef71a3949115b164bea7507c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d305f54aad2b8db44d03474e5155cfaf30dd8a8b5c5dabdca82a0a250ff1c2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dcac7d4d68c69b3693e8d1b796cb529cdb38fb41555613d24b0a7e38a92b74`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f812e356d565c8c4ec8076932f10549407639030260c467c96d4726a883439`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04959ff06f5315ca730a9cfba712a8e00d2221a04c13033809e71ea267bb2a3`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 120.5 MB (120547601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5631ad910a888b82aba59d281fc1fc1079c79e09e2346a8ab856b1a0556fe22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c07f786945aca5d5765d68743176fa83270336aa5d168d010162cca2656851f`

```dockerfile
```

-	Layers:
	-	`sha256:bd8c88a2e52536f1eb3df93ac96797c4161d0b9a9971ccf07be4bcb4e0f40d14`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 2.5 MB (2480756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae104f3c9997741edf1dbac1ba0e551642990ca6c212fb2b96d27c6763b6d4`  
		Last Modified: Tue, 30 Jan 2024 01:05:41 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-enterprise`

```console
$ docker pull neo4j@sha256:1c58c06aa26b49a7548c046d9838d647e8abeb9778328422e8af21d82df74f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7f57d28b4204c65ce716451f63e47d371e553222221cbb94b58273c9bffecc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402496166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11fd4052b4a057a45f22606fa41fe93f44ef48307e75a309b37f0be943e8204`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8959ff830f40bd981a6656c70c62d82e57efb7264dc98efd67d3ef1e5901b5d4`  
		Last Modified: Mon, 29 Jan 2024 22:52:40 GMT  
		Size: 145.3 MB (145271190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4262a7cc67cc0be1b04687679f1122ec38ea86bb5e0019be8b62d9f5315f48e4`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3922c318378bb4724fa889bdd01f68f91af6aa6567400b7f25f4dd058e1358`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfa46e8d6bfe31392cd41dda090b456c6dd5fb63a344ccb5e71bf642b7f6e9e`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 225.8 MB (225793771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0238794400af57589b4ea6dce6d190d14767c9dac25e67b3c5067f79e47c9a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fc5837110e4b5fcbaf01c724f39e06910c77826092b4c0e72c3639f8d0848c`

```dockerfile
```

-	Layers:
	-	`sha256:0afe6dd5108fd5e8ccb1dd4dadbd0611dbfa83ac00c8707413943a1d2f83472d`  
		Last Modified: Mon, 29 Jan 2024 22:52:37 GMT  
		Size: 2.6 MB (2598523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c909219396711881c16766588a7cf0fefe4087c534bcd49e4bc78f118352780e`  
		Last Modified: Mon, 29 Jan 2024 22:52:36 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f84d4f4aef9182214e0dac1dacc883e7e26a77769702b6b00e1c87e2c725f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397841376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75ae9a21f54f187d746da19c1cc7e930fde90618063400755dbebed3561b08e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a13170102bdd75bc9f73b9a27ef0e1b1a9ba8f535a97965035480c6bec4c96`  
		Last Modified: Tue, 30 Jan 2024 01:05:45 GMT  
		Size: 142.0 MB (142006635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef3ca9ea8731e04c8da5e442141e100681554eae5d28f751ac4dc01d10908d2`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aec422c866c88ef0ccd93a37e679734bb6c8863671cf949555337df4409783`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541772c0b1ddf548665c4641467e804578c562cfc3976838edff3f8b4ccab3b8`  
		Last Modified: Tue, 30 Jan 2024 01:06:51 GMT  
		Size: 225.8 MB (225757447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b8b597a08e8b2dec316a0ca3c7b8f16854766be938793d74b5b375bb32b38a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5988385128dc2563c31f60325731259e1aa7a35f54b201b496d37a8a85e3c925`

```dockerfile
```

-	Layers:
	-	`sha256:6d53dbb39ab119cd04300c99bdf29f270c820e59105cb460e00400ab528680bb`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 2.6 MB (2598845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de2fd26631fd07f06983d27c955efd6379f4a4cd4b301c312d15c0a4dc82964`  
		Last Modified: Tue, 30 Jan 2024 01:06:46 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:da5c4fe902d6353d41c89fabbaefb2047bb4083d35d33d293a21cc170da61ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:55c450fea6c35117ab581b99ab2b39cbc0fce70094231b0d913bbaf78d462dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560022021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871c8f6a84384ab56d260451ab89c15f7cf3a4188c6320071d0af9ffd8884575`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be303146fcc369d031cab05a10e11c221f44bbe25a73a30a70c2756631015f9`  
		Last Modified: Mon, 29 Jan 2024 22:53:00 GMT  
		Size: 152.2 MB (152169583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12566ca2d89ca7025e989f66218015bb13a53d1bd3ff35729385a043ad3057`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab5d91da17112dd1a8e276cae5d200fbfb8ddf704c9f7874a71a5dec4d4a81`  
		Last Modified: Mon, 29 Jan 2024 22:53:05 GMT  
		Size: 368.5 MB (368496387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:df886acaebefc57fb8294eb3437bad611b2d38a5cacdcd0bd92db337c65d5419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9014335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc46b6848e0265755eef676e8b800c0c6e41529e6796a021fd95f918418230`

```dockerfile
```

-	Layers:
	-	`sha256:1e007a89299b4246fa529ddf91d232b73f0418325f551b0532f8f950db8fd4dc`  
		Last Modified: Mon, 29 Jan 2024 22:52:58 GMT  
		Size: 9.0 MB (8994098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d407e360281b7099565d64f28d141f18496d3673e785e4fa595aaa8e0eb839f`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1caa069722d06be5dd63f830459bd4f1f1fd4b55187543e36f39e785ab3fb1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556882390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1fc341701316c6ca2b9926cba09148b7e17835fe093674e7136638b9dd2b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a17ff2795dc8d10b53d2062e9e984c5c8a4cb0e9e7ed563b9ed8e898da5bd`  
		Last Modified: Tue, 30 Jan 2024 01:04:30 GMT  
		Size: 368.5 MB (368496362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d1f5b9e6daedf00f0de7a2f15f533969bf269b7cc49715d3538269708e156b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b618d6a89ed5a87e158d868cb414347685f08f88654008f0ba5c390b6c406`

```dockerfile
```

-	Layers:
	-	`sha256:fa6c4db9e641e8fe14c13044fae1110f5bc95996ad4d9a3c118f24ee085d0ccb`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 9.0 MB (8992060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c53ae622cb3bb17ddf04066ef76fdb6b955bdff90b9f47e65e51e63290cbaa`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:da5c4fe902d6353d41c89fabbaefb2047bb4083d35d33d293a21cc170da61ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:55c450fea6c35117ab581b99ab2b39cbc0fce70094231b0d913bbaf78d462dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560022021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871c8f6a84384ab56d260451ab89c15f7cf3a4188c6320071d0af9ffd8884575`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be303146fcc369d031cab05a10e11c221f44bbe25a73a30a70c2756631015f9`  
		Last Modified: Mon, 29 Jan 2024 22:53:00 GMT  
		Size: 152.2 MB (152169583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12566ca2d89ca7025e989f66218015bb13a53d1bd3ff35729385a043ad3057`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab5d91da17112dd1a8e276cae5d200fbfb8ddf704c9f7874a71a5dec4d4a81`  
		Last Modified: Mon, 29 Jan 2024 22:53:05 GMT  
		Size: 368.5 MB (368496387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:df886acaebefc57fb8294eb3437bad611b2d38a5cacdcd0bd92db337c65d5419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9014335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc46b6848e0265755eef676e8b800c0c6e41529e6796a021fd95f918418230`

```dockerfile
```

-	Layers:
	-	`sha256:1e007a89299b4246fa529ddf91d232b73f0418325f551b0532f8f950db8fd4dc`  
		Last Modified: Mon, 29 Jan 2024 22:52:58 GMT  
		Size: 9.0 MB (8994098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d407e360281b7099565d64f28d141f18496d3673e785e4fa595aaa8e0eb839f`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1caa069722d06be5dd63f830459bd4f1f1fd4b55187543e36f39e785ab3fb1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556882390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1fc341701316c6ca2b9926cba09148b7e17835fe093674e7136638b9dd2b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a17ff2795dc8d10b53d2062e9e984c5c8a4cb0e9e7ed563b9ed8e898da5bd`  
		Last Modified: Tue, 30 Jan 2024 01:04:30 GMT  
		Size: 368.5 MB (368496362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d1f5b9e6daedf00f0de7a2f15f533969bf269b7cc49715d3538269708e156b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b618d6a89ed5a87e158d868cb414347685f08f88654008f0ba5c390b6c406`

```dockerfile
```

-	Layers:
	-	`sha256:fa6c4db9e641e8fe14c13044fae1110f5bc95996ad4d9a3c118f24ee085d0ccb`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 9.0 MB (8992060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c53ae622cb3bb17ddf04066ef76fdb6b955bdff90b9f47e65e51e63290cbaa`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:da5c4fe902d6353d41c89fabbaefb2047bb4083d35d33d293a21cc170da61ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:55c450fea6c35117ab581b99ab2b39cbc0fce70094231b0d913bbaf78d462dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560022021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871c8f6a84384ab56d260451ab89c15f7cf3a4188c6320071d0af9ffd8884575`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be303146fcc369d031cab05a10e11c221f44bbe25a73a30a70c2756631015f9`  
		Last Modified: Mon, 29 Jan 2024 22:53:00 GMT  
		Size: 152.2 MB (152169583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12566ca2d89ca7025e989f66218015bb13a53d1bd3ff35729385a043ad3057`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab5d91da17112dd1a8e276cae5d200fbfb8ddf704c9f7874a71a5dec4d4a81`  
		Last Modified: Mon, 29 Jan 2024 22:53:05 GMT  
		Size: 368.5 MB (368496387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:df886acaebefc57fb8294eb3437bad611b2d38a5cacdcd0bd92db337c65d5419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9014335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc46b6848e0265755eef676e8b800c0c6e41529e6796a021fd95f918418230`

```dockerfile
```

-	Layers:
	-	`sha256:1e007a89299b4246fa529ddf91d232b73f0418325f551b0532f8f950db8fd4dc`  
		Last Modified: Mon, 29 Jan 2024 22:52:58 GMT  
		Size: 9.0 MB (8994098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d407e360281b7099565d64f28d141f18496d3673e785e4fa595aaa8e0eb839f`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1caa069722d06be5dd63f830459bd4f1f1fd4b55187543e36f39e785ab3fb1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556882390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1fc341701316c6ca2b9926cba09148b7e17835fe093674e7136638b9dd2b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a17ff2795dc8d10b53d2062e9e984c5c8a4cb0e9e7ed563b9ed8e898da5bd`  
		Last Modified: Tue, 30 Jan 2024 01:04:30 GMT  
		Size: 368.5 MB (368496362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d1f5b9e6daedf00f0de7a2f15f533969bf269b7cc49715d3538269708e156b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b618d6a89ed5a87e158d868cb414347685f08f88654008f0ba5c390b6c406`

```dockerfile
```

-	Layers:
	-	`sha256:fa6c4db9e641e8fe14c13044fae1110f5bc95996ad4d9a3c118f24ee085d0ccb`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 9.0 MB (8992060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c53ae622cb3bb17ddf04066ef76fdb6b955bdff90b9f47e65e51e63290cbaa`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:da5c4fe902d6353d41c89fabbaefb2047bb4083d35d33d293a21cc170da61ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:55c450fea6c35117ab581b99ab2b39cbc0fce70094231b0d913bbaf78d462dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560022021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871c8f6a84384ab56d260451ab89c15f7cf3a4188c6320071d0af9ffd8884575`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be303146fcc369d031cab05a10e11c221f44bbe25a73a30a70c2756631015f9`  
		Last Modified: Mon, 29 Jan 2024 22:53:00 GMT  
		Size: 152.2 MB (152169583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12566ca2d89ca7025e989f66218015bb13a53d1bd3ff35729385a043ad3057`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab5d91da17112dd1a8e276cae5d200fbfb8ddf704c9f7874a71a5dec4d4a81`  
		Last Modified: Mon, 29 Jan 2024 22:53:05 GMT  
		Size: 368.5 MB (368496387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:df886acaebefc57fb8294eb3437bad611b2d38a5cacdcd0bd92db337c65d5419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9014335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc46b6848e0265755eef676e8b800c0c6e41529e6796a021fd95f918418230`

```dockerfile
```

-	Layers:
	-	`sha256:1e007a89299b4246fa529ddf91d232b73f0418325f551b0532f8f950db8fd4dc`  
		Last Modified: Mon, 29 Jan 2024 22:52:58 GMT  
		Size: 9.0 MB (8994098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d407e360281b7099565d64f28d141f18496d3673e785e4fa595aaa8e0eb839f`  
		Last Modified: Mon, 29 Jan 2024 22:52:57 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1caa069722d06be5dd63f830459bd4f1f1fd4b55187543e36f39e785ab3fb1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556882390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1fc341701316c6ca2b9926cba09148b7e17835fe093674e7136638b9dd2b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a17ff2795dc8d10b53d2062e9e984c5c8a4cb0e9e7ed563b9ed8e898da5bd`  
		Last Modified: Tue, 30 Jan 2024 01:04:30 GMT  
		Size: 368.5 MB (368496362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d1f5b9e6daedf00f0de7a2f15f533969bf269b7cc49715d3538269708e156b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b618d6a89ed5a87e158d868cb414347685f08f88654008f0ba5c390b6c406`

```dockerfile
```

-	Layers:
	-	`sha256:fa6c4db9e641e8fe14c13044fae1110f5bc95996ad4d9a3c118f24ee085d0ccb`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 9.0 MB (8992060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c53ae622cb3bb17ddf04066ef76fdb6b955bdff90b9f47e65e51e63290cbaa`  
		Last Modified: Tue, 30 Jan 2024 01:04:21 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:03c6aba4fff06763a73711cdb65929a152ff3364ab9965e0466dcbd11cd99ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:e5876366b42243198d0aaf4a64d761b4d9acbc65d5233b94af6f24889261fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303999503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580df611d5ec430f82d0c55146ac50c5c31c1e99104567a8a927827810b6c92c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e8a73b67a87ff4b48e7c7a850b6a1c512bc1112c8abdcd3acf2ba0308ee00b`  
		Last Modified: Mon, 29 Jan 2024 22:52:42 GMT  
		Size: 152.2 MB (152170970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a35ce891508308b07e558ccae7c34ad5d5f6c12dbee5810c8761c2eebc186c`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1954bd7427fda134feb66277824281ceb22922664b3d38245ed66e2798c70da4`  
		Last Modified: Mon, 29 Jan 2024 22:52:41 GMT  
		Size: 112.5 MB (112472482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c85616a832adc86b6c26bac4c9746368118d231bff1cec2f0ff20cef01fb77e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119aa75ca671da3f8926dfe86b41a73f0765192036735a8545c452886657dec8`

```dockerfile
```

-	Layers:
	-	`sha256:0e8a61817b9e8e7114106fc2a5dedd418322662d978df4cca387ba7e7f440b2b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 8.8 MB (8807626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5364f2c2f52334dc43ac0631a06cf4fb76c0fbece7e2ab1ecd9f7a4e1f52d8`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d430b3d7a0a4b139248f053b1785fce54e5e7c2d5061fe9afe19f0d89dd2502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b24ceb8c909cf209963e7fca3fe06063049c194518911226b0ec110005a130a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74029d795860413895920afa9e775e383fb8ab36502a3f92c886fa6db00ae5`  
		Last Modified: Tue, 30 Jan 2024 01:03:25 GMT  
		Size: 150.7 MB (150723669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6461819cbb1d17881c50a22c7a155e917b4b3aa4cbc38cd72eda9da741cc25c`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b19e25470f95c50631055502e07273df75a3dd9c2f98914668ce508d6caf57`  
		Last Modified: Tue, 30 Jan 2024 01:03:24 GMT  
		Size: 112.5 MB (112472459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:41f46b5aa7bcb3a52cbc45a4b702e35269d72266ad5ffb832d7aa50a59f7c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac71bbf5da1c5f9846bacd5d871ef4c01ebf184fe54b662a15ccbecf58ff525`

```dockerfile
```

-	Layers:
	-	`sha256:b25a2967fda321853e3fe688734e87299821f9fbe9350fcd9a28bba6b1be794a`  
		Last Modified: Tue, 30 Jan 2024 01:03:22 GMT  
		Size: 8.8 MB (8805596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b27d318e0ff370f9abcb405122e4491cbb2318b746fc6e9bd9ba91f8bf9e00`  
		Last Modified: Tue, 30 Jan 2024 01:03:21 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json
