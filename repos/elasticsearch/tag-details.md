<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.18`](#elasticsearch71718)
-	[`elasticsearch:8.12.1`](#elasticsearch8121)

## `elasticsearch:7.17.18`

```console
$ docker pull elasticsearch@sha256:3c5a456d9705300db7e85f04b0e2f54acb3b2b434b7bb6c4011eddb0b9192607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.18` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6a5008200e24d6d42a419a7bd40c25e4aec2e22f20994b3337b3545c2e4f1b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364221795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa62642b8d51b1f20c7705c549edd05d29b179db7e57b095312ceb1cfd47ecf7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-02T12:04:59.691750271Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-02T12:04:59.691750271Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c89bcdb63436b9d52a0a5401688bb9d302ffff5a19f7ac84f240a8721ced16`  
		Last Modified: Tue, 06 Feb 2024 20:52:25 GMT  
		Size: 7.5 MB (7509787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824b7aad3af79db3f5b029ba57ace65ed9e56f4dd1aca521c7792e1a6c90c73c`  
		Last Modified: Tue, 06 Feb 2024 20:52:25 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61e19e9b6d0c6341ba371a2f74f09cd3ea16ea9dc6d266a0957f2fb2b6beabb`  
		Last Modified: Tue, 06 Feb 2024 20:52:29 GMT  
		Size: 328.9 MB (328879438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4650d4f2182370871a78c5b3b463f45b5448566e3e607e485ad4adfd2d10ecde`  
		Last Modified: Tue, 06 Feb 2024 20:52:25 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9952717f8d094b1ab66b050c9a05679bbe50dde47f8043a2f00e5fd77d3854d5`  
		Last Modified: Tue, 06 Feb 2024 20:52:26 GMT  
		Size: 2.0 KB (1975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d5bda2002f822b1613a57273596e484e35693f4b6e92db0853051ded0ce75`  
		Last Modified: Tue, 06 Feb 2024 20:52:26 GMT  
		Size: 192.1 KB (192142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeeaa4094b3c1f4f52d74dd3ce013e43b0304aa6391dfddd8c0fb540ca340e`  
		Last Modified: Tue, 06 Feb 2024 20:52:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5d185922db0c6f94753e53e62ae0fae3cade7743e4826b03dae614e98617be`  
		Last Modified: Tue, 06 Feb 2024 20:52:27 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.18` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:530adef82d53d5da9573ab1c0fe33f49f25f81e739e79dc8966fd0fabf347020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2111366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea02881c06f55828201331045b9c56e16f47bce467525fce43ca0d756d43369e`

```dockerfile
```

-	Layers:
	-	`sha256:c07e797f6b27c724c32938c894df08cada6b60ee052fd4a4042c34459c7b866d`  
		Last Modified: Tue, 06 Feb 2024 20:52:25 GMT  
		Size: 2.1 MB (2073624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b3f36c67c838ad295659a52f84ad11393422c525109307e160e90cd80f6dff`  
		Last Modified: Tue, 06 Feb 2024 20:52:25 GMT  
		Size: 37.7 KB (37742 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.18` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d880835979209e68c960c9688fd6ccdff42f7428d93c839e2b96220f4a50fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360390555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80789633bdf148ad39948455ca2e094354a748455a5dddc528bc224c9def3fa6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-02T12:04:59.691750271Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-02T12:04:59.691750271Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d4c2b87a53ae05073db1e549a497aaadab7083e7376fb16c0884a05e4f9d8`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 7.3 MB (7328596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159b8ae36baed42e8be2dfb6aff2e12ffadada674ae811498b9c4ff306f98a7`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d173a2008214885944ff13ba2f2adc23bb2ebfd2fc32f7a79f19557b5cf019`  
		Last Modified: Tue, 06 Feb 2024 21:38:54 GMT  
		Size: 326.8 MB (326775081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8330c0bdb51da9614a667fad0e026357a0c66047aefa629e120e1ec2a492e1e7`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8d7c2b10f2fd94e3a7b6807dd7b57005bf8e2d025d4c5880c8b0b14acece6`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5cee5442c51836394b1cda27917ea401865c13bc1c6c465ccef1a8bbdb7935`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 186.2 KB (186171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec18c76f929475458e4b6e248d56cd1ebd2081be349bc5901a363f010722997`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9c7615c9b1c8a4af79fb6e4781c52ca3e1443a78d0ebe22e8e53eb15a3cd89`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 109.3 KB (109260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.18` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c9b90d3501c8a56cdcba3cbfe255599f687493cf02d75d93413c693fc91012fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2111532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e36eab3af58734eed9532fe187385436171518137023dcde9860c69b83f42a6`

```dockerfile
```

-	Layers:
	-	`sha256:f89c3d2f2bbae19979c9a56f353a24e7db4e2200f7af11d99efdd2b97640082c`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 2.1 MB (2073947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2f63f0e40f6a68d3da4cbeea8c2ca2826ee45bb49c25b67bc97655ae29a329`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.12.1`

```console
$ docker pull elasticsearch@sha256:8c18a68f086b0935c56a7d6fb02e602fc0e2265a31668c6679c7d159a302b1c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.12.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f9a807ef8f888a9d3f9ab680bbb8917869e66d30b3d2f086eca796545040a2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.7 MB (663720019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200ee1875d3cb0b71e7f799c83d3820552c4d8a5915e509b8c21f320066cfd69`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:33 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:33 GMT
LABEL org.label-schema.build-date=2024-02-01T13:07:13.727175297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=6185ba65d27469afabc9bc951cded6c17c21e3f3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.1 org.opencontainers.image.created=2024-02-01T13:07:13.727175297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=6185ba65d27469afabc9bc951cded6c17c21e3f3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.1
# Tue, 06 Feb 2024 11:29:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:33 GMT
CMD ["eswrapper"]
# Tue, 06 Feb 2024 11:29:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e8abd3490e6bd203e1e222c10da23199724023cb4cb975ab0cd8a51e6d1a3`  
		Last Modified: Tue, 06 Feb 2024 20:53:24 GMT  
		Size: 7.5 MB (7509819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34e4e050e9b032dd88c5b26a7d459a69f34717ada9d6498798ebda52bbc3100`  
		Last Modified: Tue, 06 Feb 2024 20:53:23 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6316470576fb4c48e0f7ae3584fc73df62397c1dd207804d7c15a07b35515`  
		Last Modified: Tue, 06 Feb 2024 20:53:39 GMT  
		Size: 628.4 MB (628378142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f790dbe9ab22d190e54db98870206249ffdb4dcb00e785f0218b7ad97dd7c`  
		Last Modified: Tue, 06 Feb 2024 20:53:24 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9c88c6df7c630184fcb5132059d635958ae9d3abd64d1ee2ff576e3cc09493`  
		Last Modified: Tue, 06 Feb 2024 20:53:25 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c925300cdd9584032da3fe89a7630be23fdc9ab83ee4530a1da122ef12890d5`  
		Last Modified: Tue, 06 Feb 2024 20:53:25 GMT  
		Size: 191.9 KB (191885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9c16a268a25342da5994689b2a33d895f6ae636dc9883b0bc1ef17d97f305d`  
		Last Modified: Tue, 06 Feb 2024 20:53:25 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaaf01d4a8aab2a12932a85ef748967779b2f4fe0e1f9a3038d26bd8e253534`  
		Last Modified: Tue, 06 Feb 2024 20:53:26 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5f25e1bf4e385293365fd7e07daec4d6cc62c8627d2820a10414030d1e0930ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5970c8e8aa1f07c7154dd5177acf80577d2ba61a7e09da3a4e4ef50646cc0ae6`

```dockerfile
```

-	Layers:
	-	`sha256:7ae1ebbc7be24ceb7e9d00bc9e704dcb80f0ac869264345acb0e20a33513f931`  
		Last Modified: Tue, 06 Feb 2024 20:53:24 GMT  
		Size: 2.4 MB (2351100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34046af67eb6bfcb11f170f02101aaac5bb0c223db8bad8c382a41732ae00643`  
		Last Modified: Tue, 06 Feb 2024 20:53:24 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.12.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b91c32efaa6ade470a07c53c4af25a6a8260e0b4e82b46834b22848ade8f52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456651193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c45e88c1762d03783c555fd19e0c0ad6fa39fe713da9fe3f204844646fb376`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:33 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:33 GMT
LABEL org.label-schema.build-date=2024-02-01T13:07:13.727175297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=6185ba65d27469afabc9bc951cded6c17c21e3f3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.1 org.opencontainers.image.created=2024-02-01T13:07:13.727175297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=6185ba65d27469afabc9bc951cded6c17c21e3f3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.1
# Tue, 06 Feb 2024 11:29:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:33 GMT
CMD ["eswrapper"]
# Tue, 06 Feb 2024 11:29:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7036eeda0b893893c3d530238575da4fe4c4ae51c9fd09e8694567e7d8780e7`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 7.3 MB (7328581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c108c9129f02502270742d354eb48ccdca567cdcf1a506749a03c9b3bf38d`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f968b80ebba231c3aca4d2e1938655c07e94445aa5405b65ea9cda6ccd8ccc`  
		Last Modified: Tue, 06 Feb 2024 21:37:33 GMT  
		Size: 423.0 MB (423036250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac5717e9155eaba2cc9d8db8bbe94d11115bedf678ec3ed1f77406e8b6d4837`  
		Last Modified: Tue, 06 Feb 2024 21:37:22 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2931a91e615c38d43e55535f2d55a95f9b860ae310217050d49ada435a566`  
		Last Modified: Tue, 06 Feb 2024 21:37:22 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec980ee4141a95cab3d7d915b3d02562dd3985c371af4592ee15d877eb7b8d54`  
		Last Modified: Tue, 06 Feb 2024 21:37:23 GMT  
		Size: 185.9 KB (185916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c4eb3e4fdd4d07711ab741c4287bccd39bd3e01fc44537e3848993ddc2628a`  
		Last Modified: Tue, 06 Feb 2024 21:37:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5701c2954bba2756d022a5d2bbe3feada32c77dc7aea20289c66c0e99072b4c2`  
		Last Modified: Tue, 06 Feb 2024 21:37:24 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:41336e90ea719b53ea981065423620349b3046a17596d4f7cb62c8c165b0d0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c514ef9601a33814550470d4dab04e8a6f9f9480451340e2d77fd6822580e47c`

```dockerfile
```

-	Layers:
	-	`sha256:76d0885bfec42e72e957d0bdc9a2d5960ff0600ee7c9cb1dfcc66ceed8b170c9`  
		Last Modified: Tue, 06 Feb 2024 21:37:22 GMT  
		Size: 2.4 MB (2351423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f81dca1bc326def90520b23653301e05fcfd26de03502be5ce3392228f2c043`  
		Last Modified: Tue, 06 Feb 2024 21:37:22 GMT  
		Size: 37.8 KB (37761 bytes)  
		MIME: application/vnd.in-toto+json
