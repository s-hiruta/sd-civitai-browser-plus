Error Leads To Extension Crash
```
CivitAI Browser+: Error: 500 Server Error: Internal Server Error for url: ValidUrl.example
Traceback (most recent call last):
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/routes.py", line 488, in run_predict
    output = await app.get_blocks().process_api(
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1431, in process_api
    result = await self.call_function(
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1103, in call_function
    prediction = await anyio.to_thread.run_sync(
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/to_thread.py", line 33, in run_sync
    return await get_asynclib().run_sync_in_worker_thread(
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 877, in run_sync_in_worker_thread
    return await future
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 807, in run
    result = context.run(func, *args)
  File "...stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/utils.py", line 707, in wrapper
    response = f(*args, **kwargs)
  File "...stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_download.py", line 220, in selected_to_queue
    model_item = create_model_item(dl_url, model_filename, install_path, model_name, version_name, model_sha256, model_id, create_json, from_batch)
  File "...stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_download.py", line 129, in create_model_item
    (preview_html, _, _, _, _, _, _, _, _, _, _, existing_path, _) = _api.update_model_info(None, model_versions.get('value'), False, model_id)
  File "...stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_api.py", line 748, in update_model_info
    for index, pic in enumerate(api_version['images']):
TypeError: string indices must be integers
```

Non-Breaking Error:
```
CivitAI Browser+: Error: 429 Client Error: Too Many Requests for url: https://civitai.com/api/v1/model-versions/2010249
CivitAI Browser+: [Warning] Unexpected API response: error
Traceback (most recent call last):
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/routes.py", line 488, in run_predict
    output = await app.get_blocks().process_api(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1431, in process_api
    result = await self.call_function(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1103, in call_function
    prediction = await anyio.to_thread.run_sync(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/to_thread.py", line 33, in run_sync
    return await get_asynclib().run_sync_in_worker_thread(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 877, in run_sync_in_worker_thread
    return await future
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 807, in run
    result = context.run(func, *args)
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/utils.py", line 707, in wrapper
    response = f(*args, **kwargs)
  File ".../stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_download.py", line 220, in selected_to_queue
    model_item = create_model_item(dl_url, model_filename, install_path, model_name, version_name, model_sha256, model_id, create_json, from_batch)
  File ".../stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_download.py", line 149, in create_model_item
    "preview_html": preview_html['value'],
TypeError: string indices must be integers
```

Cancel All Error:
```
Traceback (most recent call last):
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/routes.py", line 488, in run_predict
    output = await app.get_blocks().process_api(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1431, in process_api
    result = await self.call_function(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/blocks.py", line 1103, in call_function
    prediction = await anyio.to_thread.run_sync(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/to_thread.py", line 33, in run_sync
    return await get_asynclib().run_sync_in_worker_thread(
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 877, in run_sync_in_worker_thread
    return await future
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/anyio/_backends/_asyncio.py", line 807, in run
    result = context.run(func, *args)
  File ".../stable-diffusion-webui/venv/lib/python3.10/site-packages/gradio/utils.py", line 707, in wrapper
    response = f(*args, **kwargs)
  File ".../stable-diffusion-webui/extensions/custom-sd-civitai-browser-plus/scripts/civitai_download.py", line 364, in download_cancel_all
    if item:
UnboundLocalError: local variable 'item' referenced before assignment
```