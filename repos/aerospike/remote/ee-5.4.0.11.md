## `aerospike:ee-5.4.0.11`

```console
$ docker pull aerospike@sha256:960e6bacf41cd5d27f7952103b9f2d5f530dc0ae13f938d8b6565f5dccea8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.4.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:a35a6131ae1493ae6424f644e8bd120debd08a78584d3fd1531dd892b64d98d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76411175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c2d0a4524c35ecfbf84e36a0233473db16eca09cd5d0de8e61e6b8dbed6b65`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Thu, 15 Apr 2021 18:19:53 GMT
ENV AEROSPIKE_VERSION=5.4.0.11
# Sat, 01 May 2021 04:47:41 GMT
ENV AEROSPIKE_SHA256=a23c586ae4fdd31f916b2dda5b7c9f86a4a529cc32b110f13fda6fa393e5be93
# Sat, 01 May 2021 04:47:59 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian9" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 01 May 2021 04:48:00 GMT
COPY file:82161ba7b6e7d24ef9aeee8b19996114e9ff71c3928086ed1e58e01e82ee76a9 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 May 2021 04:48:00 GMT
COPY file:11988df14ff2f0260ab7b8ccb322ee2d343b55791c51356df1d99639d16a6dbc in /entrypoint.sh 
# Sat, 01 May 2021 04:48:00 GMT
EXPOSE 3000 3001 3002
# Sat, 01 May 2021 04:48:00 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 01 May 2021 04:48:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4df65c3c38739057be36b60930be6e0654c5081ecee88ecfbf15b8e47ebb3e`  
		Last Modified: Sat, 01 May 2021 04:48:41 GMT  
		Size: 53.9 MB (53880795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc1c3d61a68d2ac3daf0f16892eb9238359d376d0a96a471fe653c74c4161ae`  
		Last Modified: Sat, 01 May 2021 04:48:33 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6185e297042683ca5f090c7c34248f6226c7b59940908b6e6904e0c7cf351cbb`  
		Last Modified: Sat, 01 May 2021 04:48:33 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
