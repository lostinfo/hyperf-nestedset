# Hyperf-nestedset

[kalnoy/nestedset](https://github.com/lazychaser/laravel-nestedset)

```
\Lostinfo\Nestedset\NestedSet::columns($table);

\Lostinfo\Nestedset\NestedSet::dropColumns($table);
```

```
class Categories extends Model
{
    use \Lostinfo\Nestedset\NodeTrait;

    public function saving(Saving $event)
    {
        return self::onSaving($this);
    }

    public function deleted(Deleted $event)
    {
        self::onDeleted($this);
    }

    public function restoring(Restoring $event)
    {
        self::onRestoring($this);
    }

    public function restored(Restored $event)
    {
        self::onRestored($this);
    }
}
```