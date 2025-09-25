## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:fee1fd937f122c29450b5371ad999918de8ea60674c4ebd0b13e1e8253ce0f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:8e8b0efaee36e18121ab7dc869fe3ee0abd1e15fbcde242c7b9f67c91e194d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121191058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc922de6f2723e8b9d5e0f6d8ac1acf23c76c9d9ca870097495dcbb248d5904`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d2b65053f412e646e84b824154bbe7dfa5e894af0253d642dd08eefcac40b0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 6.7 MB (6665962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a974fc6c3be5853d851c4367678b3169e8bfc40e4136ec075f865ab903d2c6f`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed8451ed99c98ccf31f9d5a56ac45437e7654f0b692b232ced6ea304183de1`  
		Last Modified: Thu, 25 Sep 2025 01:12:05 GMT  
		Size: 84.8 MB (84797518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf28c19a8e2f63583616a1371baac7224ce0aa8039aefdbffcc14943f2ba12`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbcad217e989b316b8d5390328e498a1c7a67c7288799a96eea414060a54ea0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:caf5e328dec6182bcb6a665df4ea084f9b6cea24fc26642b4d3d44f9225fb153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c5bb899fbf546577b5574ac6892f51c5329bf86779b69e40d94337327ad702`

```dockerfile
```

-	Layers:
	-	`sha256:53749ce6fb588cb7c4356dfb8371a918c17514d4ee9d88e47f92aec9beafdff5`  
		Last Modified: Thu, 25 Sep 2025 02:22:28 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef91f4467414786cdf25738378986deb0f9d7405fc99ff64ebc67cbf6d0455a`  
		Last Modified: Thu, 25 Sep 2025 02:22:29 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
