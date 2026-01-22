## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:bc91ee5252592a3cd9756f274b1c788f26230ac86d0eb66ee067b4fa4c48a3ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:d32324edbb2d7371789505c7aa053e36485203449e6e7efbadeba85f9f0c8be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1671aee3d2d0dfbfd0b035eee3637b879724766c5f7f6c2c97bb78e54b57c1c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:02 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6c84e91cddc1976aed7d435e80b8655fed8d82b93a56d0f36679209d5445d6`  
		Last Modified: Tue, 13 Jan 2026 01:16:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f0dcc67dc91df789e3b57053e7bbe40566adfd7814850ef4a3b754801c4ed62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75df5161a6756c4fa0d50515d2629a154d910d55b000e735adda48cf646592b3`

```dockerfile
```

-	Layers:
	-	`sha256:dd333798adb36a8ef40bbc4c32f440889d13cba63f49be2942bfc8c8a389eb82`  
		Last Modified: Tue, 13 Jan 2026 04:24:38 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7912a2349f14ec49491d33115651b8c185e7db4e271f2be34f3e8a7fa76d19`  
		Last Modified: Tue, 13 Jan 2026 01:16:08 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0e3898781ef46ac92fcd2a01e18a08ff8abcd59212637c8924b3e75b0bddce7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e89f64a94b92c1da163e3d38bb0416d9c2fe4c583ece180778b96d63c9f44c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3328d590af06d44e564f37191fbae5238775007425643c6f6e4f3136ae883b75`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 46.0 MB (46016731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf0c94c687ae77fbf187e1cf4abb5b3bfac61c1ba1749af9c9303eb8fdfcb25`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:41477baa7e8c86f9f714e4f7bcca60e33a621cc70fa9d0fd403cd5defb23bf0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdfa82c0950f1cce66785e4e1eee882f08426648f08ffded42afe1a7a0a5e8`

```dockerfile
```

-	Layers:
	-	`sha256:2a09d10c53d9db4914542e2950f8b9a1d6d2e14350614cf739bbcb943ac12d99`  
		Last Modified: Tue, 13 Jan 2026 04:24:44 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aaf5dbd02bf6545d045c669f1b235853dc3045f8d5c770e2f1391b12bd815aa`  
		Last Modified: Tue, 13 Jan 2026 01:16:23 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:35bc203fcc08a232427483607064f909f8494199d9d09b1c401c1dec40a21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44199070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cc8b7d0e071ee01587601d02a73f58c03f16c56b67fed29869728a5dc2a28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac5d530195f102fee7fdef0edb5d3b439a9285d966c2f2c4200c53952bbeb25`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5ef928fca366eb54bbec65fa561f6860287442d04ec1dc69011f40e5f41c1f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a51eb7981323751b0e504a6bb4bd592782874f63761a0f31d56bc237a52b2e`

```dockerfile
```

-	Layers:
	-	`sha256:af5140998cba43cd8a35667fdf88267e6870a2cad9b71302a9f0dc348d7be3c7`  
		Last Modified: Tue, 13 Jan 2026 01:17:37 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758bac7b2921efcda0ee3e8d97fcc4f41a11c504c8a895a74b010d165ff2d59d`  
		Last Modified: Tue, 13 Jan 2026 04:24:50 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6e2d8d9cb6f86cff278b9ccec826c1b804dcc9bd284a5d60ba6f73fd8efa35ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48366296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a8fba16bb9f94680299194bd5224057aa82b568b15c3d75997e42e100c4de0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9930928072acb2da033d0bfddcb0bf219948b1d68ab4c4ea0da858f79479f`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fdd29f826f8941a15a9b9345b9bf630cad996ff91c300b7eb272f28d507679fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b343b98cb71795873a710c5eb9c8e081774bf58fd7591b14006a3beba762f`

```dockerfile
```

-	Layers:
	-	`sha256:6e4f2d94fdeaa61a3b6e2102be524e19a2b2ac85d9d4664114daf09df95764f3`  
		Last Modified: Tue, 13 Jan 2026 04:24:55 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb24d970e07654bbf55502c8ce45690a4091655772e3a42283a053f599f67e8f`  
		Last Modified: Tue, 13 Jan 2026 04:24:56 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:160a0e77795d2434c947a2b098eadf44f99a9717ca9674b2a6245a7ca7aab015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49468818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053655ad48bdcd118af2397d7049ad4927798e412ca67f997f81f6035ae926f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08715f1abb2de7c3214e50fa7d9445e0e80f2cd912e4f31c4bb06615b2770fc2`  
		Last Modified: Tue, 13 Jan 2026 01:16:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:51cfd36f674684bf36e6c2cf7e4f840db7576660c087f0f60e69bb746ba6366b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf9da44780550f0353037db0781dc80683dce22c754d6f2da1bcd8a9bc16c6c`

```dockerfile
```

-	Layers:
	-	`sha256:80503323239cfa111a08afbe6c3cbf913c50374d312260f3a492f2dafbb69269`  
		Last Modified: Tue, 13 Jan 2026 01:16:08 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfa42b602046401f1802da7b4175c7ed716ede7ebe027b589eda5a078138ce1`  
		Last Modified: Tue, 13 Jan 2026 04:25:10 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a73970c4f9ee22eb70a89c8a5aa7a807d7a3c3f86384902f664d21c4468b5aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48763618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fedbaa3a33c1e2dfd57df9c2e76a9bcb935a8d77e832fee712a4b7a0ae83f60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:15:41 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b9490818b8701c2761c98832197b58202569adc98ec7f32c9bb8521c888b4b`  
		Last Modified: Tue, 13 Jan 2026 01:16:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3df3ae6116f20251e3c86887d4f180b7f99c9a14217686e918b542e9f4c696e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cd1289ded9946554867793278f9be637fcecb8ac5e59f625f6b39e83ceb871`

```dockerfile
```

-	Layers:
	-	`sha256:e7e8fc19e5ad3f25b7c080844467859796e817db7f1bff2089910dcf67903a34`  
		Last Modified: Tue, 13 Jan 2026 04:25:15 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a796c3406484ae8f946b2567468af6eea264d4f1d49ecf856d26d31500e12d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62918f85cd6156ce62ec6e162845df1fc1cb00fcf3e0f4cfbe540fdcbce28090`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:14:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd02998ba54b6ca231cc34f1b7bc2f8f5c99362e4bd90f9dcffc4023f040c84`  
		Last Modified: Tue, 13 Jan 2026 01:14:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:554e5d05099f269554c630333cd96c58daebcdb395b28162b5b999553ab6855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacb2bff8853df76e3f2716a7a8aa6bd109d194194a5281d3ebcfde121bd8bf2`

```dockerfile
```

-	Layers:
	-	`sha256:03ec43ce06a7d5469cdd4401096dbef9eb572b7ff79cc01dffe4b11fc6a918bc`  
		Last Modified: Tue, 13 Jan 2026 01:14:47 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09958554c731ce028f6b5c5eeae5a5160818423462bb76e8dda619b94afbeb22`  
		Last Modified: Tue, 13 Jan 2026 01:14:47 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:020a810509d437becb2df9bd6006e0157edd408e36419045833f788310b43715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da95b8333894ce9126fbb0a39d86a16341002f07b3770a2ec0490b700c56b256`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:15:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc9f7e2f0fe7e1838188582ce7fc909a18b5a4a9abd9d38197942736909e491`  
		Last Modified: Tue, 13 Jan 2026 01:15:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e423c76a0817b5c7ef244ef553315495d1378b7538ff4ef0f8ac746b12099eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2230c8548a4437bceada6ac8169295b0889fccb46721fed755afc17b09b8ee`

```dockerfile
```

-	Layers:
	-	`sha256:f6fb8e5cdba00d86da54a1776b546de549abc577e941b9e76658b00a13de3cec`  
		Last Modified: Tue, 13 Jan 2026 04:25:23 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e996533d26d2607b770d6efcbeded7ad46e60b6c21236cad91ee7baef5198b`  
		Last Modified: Tue, 13 Jan 2026 01:15:12 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json
