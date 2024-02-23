<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.18`](#elasticsearch71718)
-	[`elasticsearch:8.12.2`](#elasticsearch8122)

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

## `elasticsearch:8.12.2`

```console
$ docker pull elasticsearch@sha256:b0dfebb1bf16b89b3cbde7f9197f13b5dd3402595a3dccb0163aa33a042a1541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.12.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f872691d805cc8d7aca4fcc3e74f99f8962d201610aa6fd55b1dd36833cd3555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.5 MB (664490485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f55cfac0970068591f7c4fe9a4f9ec2190be802dbc1efe3b60fd53942230a1`
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
# Thu, 22 Feb 2024 12:50:52 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T10:04:32.774273190Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=48a287ab9497e852de30327444b0809e55d46466 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T10:04:32.774273190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=48a287ab9497e852de30327444b0809e55d46466 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["eswrapper"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f662fbb3258f63f20fa425230dcce2b6fd249002eb9b294dbc7da505ee9ad2`  
		Last Modified: Thu, 22 Feb 2024 23:51:12 GMT  
		Size: 8.3 MB (8290646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8586f89ffdaeb4cf4eb4c4d7e82b0b719474631bf3610409646e0905bc4523`  
		Last Modified: Thu, 22 Feb 2024 23:51:11 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2fd5a8f4635b73e358c3a2d7f717a0baec0130090ac35f3821d1692d324cf3`  
		Last Modified: Thu, 22 Feb 2024 23:51:20 GMT  
		Size: 628.4 MB (628367761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0d897900d2280a7cf9d73bc3481b6c8ffe3f7fc659a8b2bd44a74b327f8a1d`  
		Last Modified: Thu, 22 Feb 2024 23:51:11 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fafddf66ad5f614b40a6d76348b28401828bbe1bfeddf53723e718bb1c7fead`  
		Last Modified: Thu, 22 Feb 2024 23:51:12 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ee318c3825648b058dea8aa86de020bd2e856c51e1bad588d5c44ac58e989b`  
		Last Modified: Thu, 22 Feb 2024 23:51:12 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b4c0532106b29048f54a86c5f5bb970bc59143433000c675ec7cfd2d9b263d`  
		Last Modified: Thu, 22 Feb 2024 23:51:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723be8f13196783cfc5d896231c38eb951850a2058adabf73e93b9cafd56dbf5`  
		Last Modified: Thu, 22 Feb 2024 23:51:13 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:20d310a01ee2a7a963ed8f74dd862f0ec7075fe97c05430000ff8bccee35b3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cce4918f9c446ce641f4d8db0cc13e9165d43624c6bc8f8fdca251261c2df1`

```dockerfile
```

-	Layers:
	-	`sha256:076432e96bb0f5f5c9957e0c3eabb2394b8fcf5b2b41c98d448e8b303ac87bd1`  
		Last Modified: Thu, 22 Feb 2024 23:51:12 GMT  
		Size: 2.6 MB (2588972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19773e68fd0a8041514bc3ff4b116e46354413dc76717ceffb8ca17d9339b0b7`  
		Last Modified: Thu, 22 Feb 2024 23:51:11 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.12.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0f7f04a6cb47287bfc1326a3e2411041a0f8de878e28a3b4a9b014e7c416c49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456650727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188e9f79ce971251d4813bb3433669173384e23df217b32f1a4859d0c4fa5d4`
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
# Thu, 22 Feb 2024 12:50:52 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T10:04:32.774273190Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=48a287ab9497e852de30327444b0809e55d46466 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T10:04:32.774273190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=48a287ab9497e852de30327444b0809e55d46466 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["eswrapper"]
# Thu, 22 Feb 2024 12:50:52 GMT
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
	-	`sha256:2ed1af1582bcbdfc15e0e37124a9ac0e29abc134def26f11f514966f0995a507`  
		Last Modified: Thu, 22 Feb 2024 23:53:01 GMT  
		Size: 423.0 MB (423035792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fab7803e220bc51b6c1e12c3b4847076d3aad1735550aa4921fbd6b5453d15`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5214107e0214f6078ffe344eac2fd5ae9a81e6f29db90fb5abbffb8ff1797211`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1189994bbdf2971d487e2f9cc481c450a2e708d17190a112ed9a9ff629bfbc9`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 185.9 KB (185910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2b1a362d38bd99c39fab367a8bf9360dbc50b441bc575fe2e5b2cc4964234`  
		Last Modified: Thu, 22 Feb 2024 23:52:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acf99084f29a4e9ce62ea5bdcb7ea15a8a5b65aebcf7ff60d4ad7431ac90ced`  
		Last Modified: Thu, 22 Feb 2024 23:52:54 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:65eec65893a1f00dd6d3bf2a4337285d8ae791fc09e2597ba2e673798564c164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754fdafc68c47235ac23187677b6b78b6e1a54ef1342bdce494ee79f9ae1ead9`

```dockerfile
```

-	Layers:
	-	`sha256:e69fa4a3a00bc8424ef49e9ad09865cfd5d9a0f3b7ae32922aab1025663c3202`  
		Last Modified: Thu, 22 Feb 2024 23:52:53 GMT  
		Size: 2.6 MB (2589189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46fb324f66000e60a058fad65d487a898dfc4f32ab0f798d86de16de6af1bb7`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
