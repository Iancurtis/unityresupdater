# unityresupdater
unity resource updater

##��Դ�Զ�����ϵͳ

###��Դ����
1. res.version
2. res.md5
3. res[]

###��ԴĿ¼
1. StreamingAssetPath ����������
2. PersistentAssetPath ���֮�����أ�

    * �����ϴ�����û��ɣ���ʱ���ļ�д��һ��������������ǣ��²�����osӦ�ö�����дdata��sync����дinode����
    * ������װʱ�ϴΰ�װ���£������絼������İ汾����StreamingAssetPath��ģ�
    * ���ܱ��û�ɾ�����գ�ȫ���򲿷֣�
    * ���ܷ��������˰汾

###Ŀ��
1. �ͻ��˶�ȡ��ȷ�汾res
2. ��Ӧ������������Զ��޸���
3. ��һ�����ذ�װ����ѹ��
4. ����û��ֹ��Ķ������ļ����ļ���С���ֲ��䣬���޸���������޸���Ҫÿ����������md5��̫����


###��������

1. VersionCheck ����res.version��res.version.latest����ȡ2��Ŀ¼version�� �Ƚϡ�

2. Md5Check

    1. ���version ��Ҫ������������res.md5.lastest����ȡ2��Ŀ¼res.md5���Ƚϣ� ɾ����md5��size���Ե�res��
       ��res.md5.lastest������Ϊres.md5����res.version.latest������Ϊres.version�� ��������ʣ���res

    2. ���version ����Ҫ��������������res.md5����Ӧ���ļ��Ƿ񶼴��ڡ��������û�ɾ�������ļ�,��2����resû��ɣ���
       �����������ɹ�������в����ڵģ���������ʣ���res

3. ResDownload����������ɺ���Ҫ�ټ���һ��md5�������Ҫ��ȫ��������ɺ󣬼�����һ�飬����һ��checked�ļ�����ǣ���ʱ�����㣩

4. Succeed

5. Failed

###ʹ��

1. using(var ru = new ResUpdater(hosts, thread, reporter, startCoroutine)) { ru.Start() }

2. reporter������UI

###TODO

1. ��Ȼ���ձ�׼��query_stringʱhttp cacheҪ����query_string ��Ϊkey���������еĿ���ṩ��û����׼��������յ��Ǹ��µ�ʱ����ļ����֣�
�����Ǽ���"?version=<md5>"�ķ�ʽ


